
pipeline{
    // need to add agents
    agent any
    
    tools{
        // here mymaven is tool configured under global tool configuration
        // new tools added
        maven 'mymaven'
    }
    
    stages{
    
        
          stage('Test Code')
        {
         
            steps{
                // you can have many steps
                sh 'mvn test'
            }
            post{
                success{
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
      
    }
}
