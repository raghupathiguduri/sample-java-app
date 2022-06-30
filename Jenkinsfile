@Library("jenkins-shared-library@kaiburr") _
pipeline {
    agent any
    tools {
        maven 'maven-3.8.6'
    }
    stages {
        stage('Checkout') {
            steps {
              deleteDir()
              echo "Checking out....."
              checkout scm
            }
        }
        stage('Build App') {
            steps {
                mvnBuild()
            }
        }
    }
}
