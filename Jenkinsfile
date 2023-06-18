pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        
        stage('Deploy') {
    steps {
        sh 'cp /var/lib/jenkins/workspace/Jenkins freestyle/target/my-webapp.war /var/lib/tomcat9/webapps/'
    }
}

        
        // Add more stages as needed
    }
}
