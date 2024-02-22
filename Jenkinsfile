pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                bat '''
                echo 'Test Step: We run testing tool like pytest here'
                
                python -m venv mlip
                source mlip\\Scripts\\activate
                pip install -r requirements.txt
                pytest
                '''

            }
        }
        stage('Deploy') {
            steps {
                bat '''
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
                '''
            }
        }
    }
}
