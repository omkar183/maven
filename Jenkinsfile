pipeline{
agent any

tools{
  maven 'Maven'
 }
 stages{
 stage('Checkout'){
 steps{
 git branch:'main',url:"https://github.com/omkar183/maven.git"
 }
 }
 stage('Build'){
 steps{
sh "mvn clean package"
}
}
stage('Test'){
steps{
sh "mvn test"
}
}
stage('Run Application'){
steps{
sh 'java -cp target/classes com.example.App'
}
}
}
post{
success{
echo'b and d'
}
Failure{
echo'f'
}
}
}
