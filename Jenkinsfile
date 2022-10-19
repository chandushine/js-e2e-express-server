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
                sh """npm install
                      npm run build
                      """
            }
        }
    }
}