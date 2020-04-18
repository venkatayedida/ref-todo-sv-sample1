pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat 'mvn clean'
                bat 'mvn package'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                bat 'java -jar -Dhost="servicev.ct.blue.cdtapps.com" -Dport="8008" ./target/ref-todo-sv-consumer-0.0.1-SNAPSHOT.jar'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
