pipeline{
agent any

tools{
  maven 'maven'
 }
 stages{
 stage(checkout){
 steps{
 git branch:'main',url:"https://github.com/omkar183/maven.git"
 }
 }
 stage(build){
 steps{
sh "mvn clean package"
}
}
stage(test){
steps{
sh "mvn test"
}
}
stage(Run Application){
steps{
java -cp target/classes com.example.App
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

