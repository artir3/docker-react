#!/usr/bin/env groovy
pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building'
                sh 'make'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
                sh 'make check || true'
                junit '**/target/*.xml'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
}

node {
    stage('Build') {
        sh 'make'
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
        echo 'Building node'
    }
    stage('Test') {
        echo 'Testing node'
        sh 'make check || true'
        junit '**/target/*.xml'
    }
    stage('Deploy') {
        echo 'Deploying node'
    }
}
