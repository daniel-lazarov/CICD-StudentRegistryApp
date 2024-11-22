pipeline {
    agent any

    stages {
        stage('Checkout'){
            steps{
               git branch: 'main', url: 'https://github.com/daniel-lazarov/CICD-StudentRegistryApp'
            }
        }
        stage("Install dependencies") {
            steps {
                script{
                    sh 'npm install'
                }
            }
        }
        stage("Start Application and run tests") {
            steps {
                script {
                    sh 'start /b npm start'
                }
            }
        }
    }

    post {
        always {
            echo 'CI pipeline completed'
        }
    }
}
