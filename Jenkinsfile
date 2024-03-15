pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add any build steps here
                
                // Copy square.pl script to workspace
                sh 'cp square.pl $WORKSPACE/'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run the square.pl Perl script
                sh 'perl square.pl'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                // Add any deployment steps here
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed'
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}

