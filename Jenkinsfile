pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                docker {
                    image 'node:19-alpine'
                    reuseNode true
                }
                steps {
                    sh '''
                        ls -la
                        node --version
                        npm --version
                        npm ci
                        npm run build
                    '''
                }
            }
        }
    }
}
