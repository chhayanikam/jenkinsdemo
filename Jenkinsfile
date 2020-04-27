pipeline {
    agent any 
    stages {
        stage('clone-repo') { 
            steps {
                bat "git clone http://github.com/chhayanikam/jenkinsdemo.git/"
                bat "mvn clean http://github.com/chhayanikam/jenkinsdemo.git/"
             // bat 'start cmd.exe /c date'
            }
        }
        stage('Test') { 
            steps {
              bat "mvn test http://github.com/chhayanikam/jenkinsdemo.git/" 
             // bat 'start cmd.exe /c time'
            }
        }
        stage('Deploy') { 
            steps {
               bat "mvn package http://github.com/chhayanikam/jenkinsdemo.git/" 
            //  bat 'start cmd.exe /c dir'
            }
        }
    }
}
