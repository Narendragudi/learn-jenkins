pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = 'Hello Jenkins'
    }

    options {
        timeout(time: 1, unit: 'SECONDS')
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
                sh """
                  echo " here i wrote shell script"
                  echo "$GREETING"
                  sleep 10
                """
            }
       }
   }
    // post-build
   post {
       always {
            echo 'I will always say Helloagain!'
       }
       failure {
            echo 'this runs when pipeline is failed,used generally to send some alrets'
       }
       success {
            echo 'i will say hello when pipe line is success'
       }
   }
}