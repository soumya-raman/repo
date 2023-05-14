pipeline
{
    agent any
    stages
    {
        stage('ContinoiusDeploy')
        {
            steps
            {
                deploy adapters: [tomcat9(credentialsId: '628282f6-6934-4b43-a987-e9711d985093', path: '', url: 'http://172.31.95.59:8080')], contextPath: 'newtest', war: '**/*.war'
            }
        }
        stage('ContinoiusTesting')
        {
            steps
            {
               git 'https://github.com/prasadcloud/FunctionalTesting.git'
            }
        }
        stage('ContinoiusDelivery')
        {
            steps
            {
               deploy adapters: [tomcat9(credentialsId: '628282f6-6934-4b43-a987-e9711d985093', path: '', url: 'http://172.31.88.195:8080')], contextPath: 'newprod', war: '**/*.war'
            }
        }
    
    }
}
