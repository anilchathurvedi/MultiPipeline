
pipeline{
    agent {label 'java'}
    environment{
       PATH = "/usr/share/maven/bin:$PATH"
    }
    
    stage('Git Checkout') {
            steps{
               
                gitCheckout(
                    branch: "master",
                    url: "https://github.com/Indianche/simplewebapp.git"
                )
            }
        }
    
    stages{
          stage("maven build"){
            steps{
                sh "mvn clean package"
            }   
        } 
        
        
    }   
}
