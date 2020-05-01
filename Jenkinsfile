pipeline {
   agent any
   stages {
      
      stage('Build image') {
          steps {
              sh 'sudo docker build -t pranavjoy/go-docker:latest .'
          }
      }
	   
      stage('Docker login') {
    	  steps {
		  sh "sudo docker login -u ${DOCKER_USER} -p ${DOCKER_PASSWORD}"
	  }
      }
      
      stage ('Push image'){
	  steps {
		sh "sudo docker push pranavjoy/go-docker:latest"
	  }      
      } 
   }
}
