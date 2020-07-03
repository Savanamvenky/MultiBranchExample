
timestamps
{
    properties([
        parameters ([
          string(name: 'BuildNode', defaultValue: 'master', description: 'Where to build'),
          string(name: 'ECSService', defaultValue: 'a204044-otp-dev1-tax-expense', description: 'AWS ECS Servcie Name'),
          string(name: 'AWSRegion', defaultValue: 'us-east-1', description: 'AWS Region')
       ])])
    node(BuildNode) 
    {
        try
        {
            
       
        def BN = "${BuildNode}"
       
       stage("checking")
       {
          echo "this stage is to check the creation of parameters: ${BN}"
       }
       }
        catch (e) 
        {
            echo e.getMessage()
            currentBuild.result='FAILURE'
            throw e
        }
     }
}
       
        
        
