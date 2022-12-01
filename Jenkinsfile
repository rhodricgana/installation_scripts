pipeline{
    agent any

    stages{
        stage("sonar quality test"){
             agent{
                  docker {
		              sudo image 'maven'
		          }
             }
            steps{
                 script{
                     withSonarQubeEnv(credentialsId: 'sonar-token') {
                         
			 sh 'mvn clean package sonar:sonar'
                    }
                }
            } 
        }
    }
}
