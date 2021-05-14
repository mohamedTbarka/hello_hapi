#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u root:sudo /home/jenkins/workspaces/arcadian'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}
