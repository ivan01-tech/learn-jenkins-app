pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                sh 'echo "Bonjour lesgens"'
            }
        }
        
        stage('w docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'echo "Bonjour Avec Dcoker"'
                sh 'node -v'
            }
        }
    }
}
