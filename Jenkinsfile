
pipeline{
    agent any
    environment{
       PATH = "/usr/share/maven/bin:$PATH"
    }
    
    stage('Git Checkout') {
            steps{
               
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master']],
                    doGenerateSubmoduleConfigurations: false,extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/anilchathurvedi/MultiPipeline.git']]])
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
