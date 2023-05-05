pipeline {
    agent any
     environment {
            CI = 'true'
        }
    tools {nodejs 'node'}
    stages {
        stage('npm version') {
            steps {
                sh 'npm version'
            }
        }
        stage('Test') {
                    steps {
                        sh './jenkins/scripts/test.sh'
                    }
                }
        stage('Deliver') {
                     steps {
                                sh './jenkins/scripts/deliver.sh'
                                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                                sh './jenkins/scripts/kill.sh'
                            }
                      }

    }
}
