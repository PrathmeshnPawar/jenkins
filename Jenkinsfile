pipeline {
    agent any

    stages {
        stage('Compile Java') {
            steps {
                echo 'Compiling Java Program...'
                bat 'mkdir out'
                bat 'javac -d out Main.java'
            }
        }

        stage('Run Program') {
            steps {
                echo 'Running Java Program...'
                bat 'java -cp out Main'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            bat 'rmdir /s /q out'
        }
    }
}
