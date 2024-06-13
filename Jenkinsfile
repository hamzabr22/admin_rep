pipeline {
    agent any 
    stages {
        stage('clone') { 
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/hamzabr22/test"
            }
        }
        stage('build') { 
            steps {
                sh "cd test/ && javac Main.java"
            }
        }
        stage('run') { 
            steps {
                sh "cd test/ && java Main"
            }
        }
    }
}
