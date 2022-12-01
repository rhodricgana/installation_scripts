pipeline{
    agent any

    stages{
        stage("sonar quality test"){
             agent{
                  docker {
		              image 'maven'
		          }
             }
            steps{
                 script{
                     withSonarQubeEnv(credentialsId: 'sonar-token') {
                         
			 sh 'sudo mvn clean package sonar:sonar'
                    }
                }
            } 
        }
    }
}
