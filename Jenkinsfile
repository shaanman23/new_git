pipeline {
    // 1. Agent: Defines where the pipeline runs. 'any' means any available Jenkins agent/node.
    agent any

    // 2. Stages: Defines the sequence of work to be performed.
    stages {
        stage('Checkout Source Code') {
            steps {
                // This command tells Jenkins to pull the code from the Git repository 
                // that you configured in the job settings.
                checkout scm
                echo "Source code successfully checked out."
            }
        }
        
        stage('Build') {
            steps {
                echo "Starting application build..."
                // Replace the 'echo' below with your actual build command (e.g., sh 'npm install' or sh 'mvn package')
                echo "Build completed successfully."
            }
        }
        
        stage('Test') {
            steps {
                echo "Running unit and integration tests..."
                // Replace the 'echo' below with your actual test command (e.g., sh 'npm test' or sh 'mvn test')
                echo "All tests passed."
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deploying application to environment..."
                // Replace the 'echo' below with your deployment commands (e.g., sh 'docker push' or sh 'scp')
                echo "Deployment finished."
            }
        }
    }
    
    // 3. Post: Actions to run after the pipeline completes, regardless of success or failure.
    post {
        always {
            echo 'Pipeline job finished.'
        }
        failure {
            echo ' The Pipeline FAILED! Review the console output immediately.'
        }
        success {
            echo 'Pipeline successfully completed all stages.'
        }
    }
}
