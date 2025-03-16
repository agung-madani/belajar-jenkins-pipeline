pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
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
