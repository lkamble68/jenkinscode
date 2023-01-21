pipeline {
    agent any
    environment {
        name = 'Laxman Kamble'
    }
    
    parameters {
        string(name: 'person', defaultValue:'Krishna Kamble', description: "Who are you?")
        booleanParam(name: 'isMale', defaultValue: true, description: "Yes, He is male!")
        choice(name: 'City', choices:['Pune','Bengaluru','Mumbai'], description: "Love my city!")
    }

    stages {
        stage('Test') {
            steps {
                echo 'Hello Test Success Laxman'
                sleep 5
                sh 'date'
            }
        }
        stage('Parameters') {
            steps {
                sh 'echo "${BUILD_ID}"'
                sh 'echo "${name}"'
                sh 'echo "${person}"'
                
            }

        }
        stage('Deploy On Test') {
            environment {
            username = 'Laxman Kamble from Karnatka'
        }
            steps {
                
                sleep 7
                sh 'date'
                sh 'echo "${username}"'
            }
        }
        stage('Continue ?') {
            input {
                    message "Should we continue?"
                    ok "Yes we Should"
                }
            steps {
                echo 'Hello Deploy On Pre-Prod Success Laxman'
                sleep 8
                sh 'df -h'
            }
        }
        stage('Deploy On Prod Main') {
            steps {
                echo 'Hello Deploy On Prod Main Success Laxman'
                sleep 9
            }
        }
        
    }
    post{
        always {
            echo 'I will always say, Hello Again!'
        }
        failure{
            echo 'Failure'
        }
        success{
            echo 'Success'
        }
    }
}

