pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello_world hello_world.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './hello_world'
            }
        }
        stage('Deploy') {
            steps {
                // Create deployment directory if it doesn't exist
                bat 'mkdir C:\\Users\\Abc\\Desktop\\SEM6\\CD\\Jenkins_lab-main\\main'
                
                // Copy executable to deployment directory
                bat 'copy hello_world.exe C:\\Users\\Abc\\Desktop\\SEM6\\CD\\Jenkins_lab-main\\main'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
