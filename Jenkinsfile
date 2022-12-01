pipeline{
    
    agent any
    
    stages{
        
        stage("sonar quality test"){

	    agent{
		
		 docker {
		     image 'maven'
		 }
	    }
            
            steps {
                script{
			withSonarQubeEnv(credentialsId: 'sonar-token') {
   			 // some block
			 sh 'mvnckage sonar:sonar'
            }
        }
        
    }
}
