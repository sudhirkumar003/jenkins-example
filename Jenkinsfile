pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                maven(maven : 'MAVEN') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                maven(maven : 'MAVEN') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                maven(maven : 'MAVEN') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
