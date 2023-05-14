pipeline
{
    agent any
    stages
    {
        stage('ContinoiusDownload')
        {
            steps
            {
                git 'https://github.com/prasadcloud/maven2.git'
            }
        }
        stage('ContinoiusBuild')
        {
            steps
            {
                sh 'mvn package'
            }
        }
    }
}
