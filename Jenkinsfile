pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'apache-maven_3_3_9'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'apache-maven_3_3_9'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'apache-maven_3_3_9'){
                        bat "mvn deploy"
                }

            }
        }
    }
}