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
            steps {
                parallel(
                    succed: {
                        echo 'success'
                    },
                    failing: {
                        error
                    }
                )
            }
        }
        stage('After') {
            steps { 
                echo 'after Parallels'
            }
        }
    }
}