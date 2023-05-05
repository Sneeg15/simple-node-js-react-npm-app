pipeline {
    agent any
     environment {
            CI = 'true'
        }
    tools {nodejs 'node'}
    stages {
        stage('npm installation') {
            steps {
                sh 'npm install'
            }
        }

    }
}
