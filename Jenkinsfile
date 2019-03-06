node {

stage('Clone Repository')
{
checkout scm
}


stage('Show me the files')
{
sh "ls -l"
}


stage('Build Docker Image and push image to DockerHub')

{
sh "docker build -t revisions:version1 ."
}
  
stage('Docker login to hub and push the image'){
sh "docker login -u 'jgit' -p 'Devops123'"
sh "docker tag revisions:version1 jgit/revisions:version1"
sh "docker push jgit/revisions:version1"
}


stage('Apply changes to the environment')
{
sh "ls -l"
}




}
