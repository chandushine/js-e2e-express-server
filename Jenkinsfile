pipeline {
    agent {label 'cancan'}
    stages {
        stage ('Clone') {
            steps {
                git branch: 'main', url: "https://github.com/chandushine/js-e2e-express-server.git"
            }
        }
        stage ('build') {
            steps {
                sh """export PATH=/home/ubuntu/.nvm/versions/node/v16.17.1/bin:$PATH
                      npm install
                      npm run build
                      """
            }
        }
    }
}