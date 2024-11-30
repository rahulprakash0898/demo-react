pipeline{
    agent any

    stages{
        stage('clone'){
            steps{
                // Clone the repository
                git 'https://github.com/VootlaSaiCharan/demo-react.git'
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

        stage('cleaning the old file'){
            steps{
                // Delete the old file
                sh 'rm -rf /var/www/html/*'
            }
        }

        stage('copy build files to the web server'){
            steps{
                // Copy the build files to the web server
                sh 'cd build && cp -r * /var/www/html/'
            }
        }
    }
}