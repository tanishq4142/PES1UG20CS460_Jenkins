pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS460-1 PES1UG20CS460-1.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS460-1'
            }
        }

        stae('Deploy') {
            steps {
                echo 'deployed successfully'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
