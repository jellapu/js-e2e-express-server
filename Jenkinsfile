pipeline {
    agent { label 'nodejs2' }
    stages {
        stage('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/jellapu/js-e2e-express-server.git'
            }
        }
        stage('installing npm') {
            steps {
                nodejs(nodeJSInstallationName: 'NodeJs18.1.0' ) {
                    sh 'npm install '
                }
            }
        }
        stage('test') {
            steps {
                nodejs(nodeJSInstallationName: 'NodeJs18.1.0' ) {
                    sh 'npm test '
                }
            }
        }
        stage('build') {
            steps {
                nodejs(nodeJSInstallationName: 'NodeJs18.1.0' ) {
                    sh 'npm run build'
                }
            }
        }
    }
}