pipeline{
    agent any

    stages{
        stage('clone'){
            steps{
                // Clone the repository
                git 'https://github.com/VootlaSaiCharan/demo-react.git'
            }
        }

        stage('cleaning the old file'){
            steps{
                // Delete the old file
                sh 'chmod -R 777 /var/www/html/'
                sh 'rm -rf /var/www/html/*'
            }
        }

        stage('installing the packages'){
            steps{
                // Install the packages
                sh 'npm install'
            }
        }

        stage('Build the application'){
            steps{
                // Build the application
                sh 'npm run build'
            }
        }

        stage('copy build files to the web server'){
            steps{
                // Copy the build files to the web server
                sh 'cp -r build/* /var/www/html/'
            }
        }
    }
}