pipeline {
    agent any 
    stages {
        stage('clone-repo') { 
            steps {
                bat "git clone https://github.com/pknowledge/my-app.git"
                bat "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                bat "mvn test -f my-app" 
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package -f my-app" 
            }
        }
    }
}
