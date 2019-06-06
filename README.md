
pipeline
{
 agent any
    
    stages
    {
             stage('compile')
            {
                steps
                {
                    sh 'mvn -f /root/.jenkins/workspace/pipeline3/mavewebappdemo install'
                }
          }
             stage ('Deploy')
    {
        steps
        {
           sh 'cp -R /root/.jenkins/workspace/pipeline3/mavewebdemo/target/* /opt/apache-tomcat-8.5.3/webapps'
        }
        
    }
        }
     }   
           
