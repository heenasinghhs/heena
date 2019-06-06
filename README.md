# heena
pipeline
{
 agent any
    
    stages
    {
             stage('compile')
            {
                steps
                {
                    sh 'mvn -f /root/.jenkins/workspace/pipeline2/mavewebappdemo install'
                }
            }
        }
     }   
           
