pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                branches: [[name: '*/main']],
                doGenerateSubmoduleConfigurations: false, extensions: [],
                submoduleCfg: [],
                userRemoteConfigs: [[url: 'https://github.com/jaswantg98/expense_service']]])
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

//        stage('Test') {
//            steps {
//                sh 'mvn test'
//            }
//        }

//        stage('Deploy') {
//            steps {
//                // Add deployment steps here
//            }
//        }
    }
}
