pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // If using a Git repo, insert checkout scm here.
                echo 'Assume files already present on Jenkins node'
            }
        }
        stage('Scale Containers') {
            steps {
                sh '''
                    cd $WORKSPACE/jenkins-scale-docker
                    ./scale.sh
                '''
            }
        }
    }
}
