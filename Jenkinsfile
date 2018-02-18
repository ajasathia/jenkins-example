pipeline {
    agent any

    stages {
        stage ('Maven Install Stage') {

            steps {
                withMaven(maven : 'maven_3_5_2') {
                    sh 'mvn clean install'
                }
            }
        }
        
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_2') {
                    sh 'mvn test'
                }
            }
        }
    }
}
