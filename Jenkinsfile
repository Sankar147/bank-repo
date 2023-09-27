pipeline {
    agent {
        label 'linux-node'
    }
    tools {
        maven 'maven_3.9.4'
    }
    stages {
        stage('fetch the code from scm') {
            steps {
               git branch: 'main', url: 'https://github.com/Sankar147/bank-repo.git'
            }
        }
        stage('build the code') {
            steps {
                sh 'mvn install -DskipTests'
            }
        }
        stage('post actions') {
            steps {
                echo "sucessfully build"
            }
        }
        stage('UNIT TESTS') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
