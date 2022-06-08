pipeline{
    agent{label 'build_java_11'}
    stages{
        stage(SCM){
            steps{
                git branch: 'main', url: 'https://github.com/jellapu/js-e2e-express-server.git'
            }
        }
        stage('install the dependencies'){
            steps{
                sh "npm install"
            }
        }
        stage('test'){
            steps{
                sh "npm test"
            }
        }
    }
}