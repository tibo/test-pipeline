pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello'
            }
        }
        stage('World') {
            steps {
                echo 'World'
            }
        }
        stage('Parallels') {
            parallel succed: {
                echo 'success'
            },
            failing: {
                exit 1
            }
        }
        stage('After') {
            steps { 
                echo 'after Parallels'
            }
        }
    }
}