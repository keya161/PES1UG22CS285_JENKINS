pipeline {
    agent any

    stages {
        // stage('Build') {
        //     steps {
        //         echo 'Building...'
        //         sh 'g++ -o hello_exec hello.cpp'  
        //     }
        // }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ -o hello_exec hello_wrong.cpp' 
            }
        }

        
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './hello_exec'  
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo "Deployment successful!"'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
