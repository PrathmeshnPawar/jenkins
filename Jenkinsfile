pipeline {
    agent any

    stages {
        stage('Checkout Source') {
            steps {
                echo 'Checking out source code...'
                // Make sure your Jenkins job is connected to the Git repo
                checkout scm
            }
        }

        stage('Compile Java') {
            steps {
                echo 'Compiling Java Program...'
                sh 'javac Main.java'
            }
        }

        stage('Run Program') {
            steps {
                echo 'Running Program...'
                sh 'java Main'
            }
        }
    }

}

