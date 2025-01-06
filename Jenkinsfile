pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/Sreeshap01/jenkins-hello-world.git'

                // To run Maven on a Windows agent, use
                bat "mvn clean package -DskipTests=true"
            }
        }
        stage('Unit Test') {
            steps {
                // To run Maven on a Windows agent, use
                bat "maven test"
            }
        }
    }
}
