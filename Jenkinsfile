pipeline
{
agent label {'ansible_node_build'}
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

  }
}
