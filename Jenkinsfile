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
            emailext body: '''<b>Example</b>
            <br>$DEFAULT_CONTENT

            <br> Note : Do not reply to this mail
            <br>
            <br>Thanks 
            <br>Automation Team''', subject: 'UI Test Result $DEFAULT_SUBJECT', to: 'lasthostel64@gmail.com'
        }
    }
}
