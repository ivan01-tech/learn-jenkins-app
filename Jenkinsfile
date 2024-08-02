pipeline {
    agent any

    stages {
        // stage('w/o docker') {
        //     steps {
        //         sh 'echo "Bonjour lesgens"'
        //     }
        // }

        stage('w docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh
                '''
                    ls -la
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
