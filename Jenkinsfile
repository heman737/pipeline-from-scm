pipeline {
    agent any
    environment {
        name = 'himanshu'
    }
    parameters {
        string(name: 'person', defaultValue: 'Heman', description: 'Enter your name')
        booleanParam(name: 'Male')
        booleanParam(name: 'Female')
        choice(name: 'City', choices: ['Nagpur', 'Mumbai', 'Pune'])
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo "${name}"'
            }
        }
        stage('Approve') {
            input {
                message "Approve/Abort"
                ok "Approved"
            }
            steps {
              echo "deploy to prod"
            }   
            }
        stage('Deploy') {
            steps {
                echo "Deployed successfully"
            }
        }
        
        }
        post {
            always {
                echo 'Always'
            }
            failure {
                echo 'Failed'
            }
            success {
                echo 'Successful'
            }
        }   
    }
