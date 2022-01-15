pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                //bat "rmdir  /s /q Practica4Maven"
                bat "git clone https://github.com/galanillo/Practica4MavenProject.git"
                bat "mvn clean -f Practica4Maven"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Practica4Maven"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Practica4Maven"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Practica4Maven"
            }
        }
    }
}
