pipeline {

agent any {

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
}
}
}


}

}


