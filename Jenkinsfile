timestamps
{
    node(build_server)
    {
        try
        {
        parameters {
          string(name: 'BuildNode', defaultValue: 'otp-stilton-ecs-build-node', description: 'Where to build')
          string(name: 'ECSRegistry', defaultValue: '367379483300.dkr.ecr.us-east-1.amazonaws.com/a204044/nonprod/tax-expense', description: 'AWS ECR Repo Name')
          string(name: 'ECSCluter', defaultValue: 'a204044-common-otp-dev1-cluster-clusterconfig', description: 'AWS ECS Cluster Name')
          string(name: 'ECSService', defaultValue: 'a204044-otp-dev1-tax-expense', description: 'AWS ECS Servcie Name')
          string(name: 'AWSRegion', defaultValue: 'us-east-1', description: 'AWS Region')
	        string(name: 'ECSContainer',defaultValue: 'otp-tax-expense-dev1-container',description: 'the conatiner name')
       }
       stage("checking")
       {
          echo "this stage is to check the creation of parameters"
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
       
        
        
