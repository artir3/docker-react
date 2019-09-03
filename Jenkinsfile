pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
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
    checkout scm
    stage('Build') {
        echo 'Building node'
    }
    stage('Test') {
        echo 'Testing node'
    }
    stage('Deploy') {
        echo 'Deploying node'
    }
}
