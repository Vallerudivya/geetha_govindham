pipeline {
    agent any

    stages {
        stage('cd') {
            steps {
                git 'https://github.com/AneesRavidKhan/DemoATC.git'
            }
        }
        stage('cb') {
            steps {
                sh 'mvn install'
            }
        } 
       stage('c dep') {
            steps {
                sh 'sshpass -p "divya" scp target/DemoATR.war root@172.17.0.3:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        } 
    }
}

