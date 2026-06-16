pipeline {
​
agent any
​
​tools {
maven 'maven'
jdk 'jdk'
}
​stages {
​
​
​
stage('Checkout') {
​ steps {
​
git branch: 'main',
​
url: 'https://github.com/1bi23cs254/MavenAppPract1.git'
​ }
​
}
​
stage('Build') {
​ steps {
​
sh 'mvn clean package'
​ }
​
}
​
stage('Test') {
​ steps {
​
sh 'mvn test'
​ }
​
}
​
stage('Run Application') {
​ steps {
​
// Start the JAR application
​
sh 'java -jar target/MyMavenApp-sam-1.0-SNAPSHOT.jar'
​ }
​
}
​
}
​
post {
​
success {
​ echo 'Build and deployment successful!'
​
}
​
failure {​ echo 'Build failed!'
​
}
​
}
}
