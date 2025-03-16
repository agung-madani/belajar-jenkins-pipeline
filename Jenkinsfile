pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                script {
                    for (int i = 0; i < 10; i++) {
                        echo("Script ${i}")
                    }
                }
                echo 'Build success'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                // sh('./mvnw test')
                echo 'Test success'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
            }
        }
    }

    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if the stage is successful'
        }
        failure {
            echo 'This will run only if the stage fails'
        }
        unstable {
            echo 'This will run only if the stage is unstable'
        }
        changed {
            echo 'This will run only if the stage changes'
        }
        aborted {
            echo 'This will run only if the stage is aborted'
        }
        cleanup {
            echo 'This will run only if the stage is cleaned up'
        }
    }
}
