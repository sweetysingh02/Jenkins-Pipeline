pipeline {
agent any
tools (
maven "maven_home"
jdk "Jdk_home"
}
stages {
}
stage('Stage 1 - INITIALIZATION') {
steps {
}
}
stage('Stage 2 - COMPILE CODE') {
steps (
}
}
}
stage('Stage 3 UNIT TEST') {
steps {
}
post {
}
}
}
input('Do you want to proceed?')
echo 'THIS IS THE DEMO OF MAVEN PIPELINE USING JENKINS'
stage('Stage 4 - INTEGRATION TEST') {
steps {
}
bat "mvn compile"
}
echo "Running Unit Test"
bat "mvn test"
stage('Stage 5 - CREATE BUILD') {
steps {
echo "Running Integration Test"
bat "mvn verify"
echo "Creating a build"
bat "mvn package"
failure {
echo "Email has been sent for Jenkins build failure"
}
}
}
  
