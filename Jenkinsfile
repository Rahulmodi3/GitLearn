pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                bat 'python Pages\\LoginPage.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    
    post { 
        always { 
            emailext body: '''$DEFAULT_CONTENT

            Note : Do not reply to this mail

            Thanks 
            Automation Team''', subject: 'UI Test Result $DEFAULT_SUBJECT', to: 'lasthostel64@gmail.com'
        }
    }
}
