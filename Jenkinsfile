pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

      //build

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
       }
   }
    // post-build
   post {
       always {
            echo 'I will always say Helloagain!'
       }
       failure {
            echo ''
       }
       success {
            echo ''
       }
   }
}