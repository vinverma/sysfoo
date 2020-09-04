pipeline{

agent any

tools {
maven 'MVN-Plugin'
}

stages {

stage('pipelinedemo') {
steps {
sh 'mvn compile'
}
}
stage('test') {
steps {
sh 'mvn clean test'
}
}
stage('archive') {
steps {
sh 'package -DskipTests'
}
}
}

}
