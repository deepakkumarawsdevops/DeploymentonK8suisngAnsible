pipeline
{
agent {label 'ansible_node_build'}
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
 stage('Build Docker image using ansible'
{
steps
{
 sh 'ansible-playbook ansible_builddockerimage.yml'
} 

}


  }
}
