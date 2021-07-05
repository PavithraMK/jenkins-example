pipeline {
    agent {label 'node_1'}

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn test'
                }
            }
        }
    }
  }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn deploy'
                }
            }
        }
    
