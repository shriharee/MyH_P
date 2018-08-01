pipeline {
agent any

stages {
stage ('Compile Stage'){
steps{
echo 'Building'
withMaven(maven : 'maven_3.5.3'){
sh 'mvn clean compile'
      }
   }
}
stage ('Test Stage'){
steps{
withMaven(maven : 'maven_3.5.3'){
sh 'mvn test'
    }
 }
}
stage ('Deplyotment Stage'){
steps{

withMaven(maven : 'maven_3.5.3'){
sh 'mvn deploy'
    }
 }
}


}
}
