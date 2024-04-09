pipeline {
    agent any
    
    stages {
        stage('Validate') {
            when {
                branch "feature/anil"
            }
            steps {
                echo 'mvn clean package' 
            }
        }
        stage('test') {
            steps {
                echo 'mvn test' 
            }
         }
         stage('Build') {
            steps {
                echo 'mvn clean install'
             }
          }
       }
    post {
        success {
            // Action to perform if Build is successful
            echo 'Build successful'
        }
        failure {
            // Action to perform if Build no successful
            echo 'Build Failure'
        }
    }
}
