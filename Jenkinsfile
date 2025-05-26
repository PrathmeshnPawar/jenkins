pipeline {
    agent any

    stages {
        stage('Compile Java') {
            steps {
                echo 'Compiling Java Program...'
                sh 'javac HelloWorld.java'
            }
        }

        stage('Run Program') {
            steps {
                echo 'Running Program...'
                sh 'java HelloWorld'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            sh 'rm -f *.class'
        }
    }
}
