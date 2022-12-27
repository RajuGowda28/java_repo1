pipeline {
    agent {
        label 'tomcat-slave'
    }
    stages {
        stage('git checkout') {
            steps {
                git 'https://github.com/Sreedevi28/java_repo1.git'
            }
        }
        stage('Build stage') {
            steps {
                 sh 'mvn install'
            }
        }

        stage('Push Artifactory') {
            steps {
                 sh 'sleep 15'
            }
        }
        stage('Deploy') {
             steps {
                 sh 'sudo cp /home/ec2-user/jenkins-slave1/workspace/tomcat-test/target/works-with-heroku-1.0.war /home/ec2-user/tom/apache-tomcat-9.0.64/webapps/'
            }
        }
    }
}    
