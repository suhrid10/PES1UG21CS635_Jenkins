pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build commands here
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here
            }
        }

        stage('Deploy') {
            steps {
                ech 'Deploying the application...'
                // Add your deployment commands here
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'

            script {
                currentBuild.result = currentBuild.resultIsBetterOrEqualTo('FAILURE') ? currentBuild.result : 'FAILURE'
            }
        }
    }
}
