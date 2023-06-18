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
        sh 'su'
        sh 'cp /var/lib/jenkins/workspace/pipeline/target/my-webapp.war /var/lib/tomcat9/webapps/'
        sh 'sudo systemctl restart tomcat9'
    }
}

        
        // Add more stages as needed
    }
}
