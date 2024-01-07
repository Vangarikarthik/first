pipeline {
agent any 
stages {
stage('Build') {
            steps {
                // Compile your Java code
                sh 'javac -sourcepath src -d build src/name.java'
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

