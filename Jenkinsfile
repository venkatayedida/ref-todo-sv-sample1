pipeline 
{
	agent any
		stages {
		stage ('Build') {
			steps {
				sh 'mvn clean install'
			}
		} stage ('Test') {
			steps {
				sh 'java-jar-Dhost="servicev.ct.blue.cdtapps.com" -Dport="8008" ./target/ref-todo-sv-consumer-0.0.1-SNAPSHOT.jar'
			}
		}
	}
}
