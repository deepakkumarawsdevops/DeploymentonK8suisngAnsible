pipeline
{
agent {label 'ansible_node_build'}
environment
{
DOCKERHUB_CREDENTIALS = credentials ('docker-hub-login')
}
stages
{
stage('Build maven project')

 {

 steps 

  {
    echo 'building'
    sh 'mvn package'
    sh 'mvn install'
 
  } 

  }
 stage('Build Docker image using ansible')
{
steps
{
 sh 'ansible-playbook ansible_builddockerimage.yml'
} 

}
 stage('docker hub login')

 {

 steps
 {
   sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USER --password-stdin'

   
 } 

 }
  stage('push docker image')

 {

 steps
 {
   sh 'docker push deepakkumarawsdevops/k83image:1'


 }
}

  }
} 

