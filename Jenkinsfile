pipeline {
    agent {
        docker {
            image 'openjdk:11' // Use the OpenJDK 11 Docker image
            args '-v /var/run/docker.sock:/var/run/docker.sock' // Mount Docker socket for Docker inside Docker
        }
    }
    
    stages {
        stage('Build') {
            steps {
                // Compile your Java code
                sh 'javac -sourcepath src -d build name.java'
            }
        }
        
        stage('Test') {
            steps {
                // Run your Java program or tests
                sh 'java -cp build name'
            }
        }
    }
}


