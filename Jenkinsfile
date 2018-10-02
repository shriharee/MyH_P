pipeline {

agent any 
  stages{
stage ('compile repo'){
steps{

withMaven(maven : 'maven'){
sh 'mvn clean compile'
}
}

}

stage('Test'){
steps{
withMaven(maven : 'maven'){
sh 'mvn test'
}
}
}

stage('Deploy'){
steps{
withMaven(maven : 'maven'){
 sh 'mvn deploy' 
sh 'cp /var/lib/jenkins/workspace/test-pipeline/target/MyH_P.war /opt/tomcat/webapps/'  
}
}
}


}

}


