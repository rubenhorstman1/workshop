Pipeline{
Agent{
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
}
Stages{
    stage('unittests'){
	steps{
	sh 'mvn test'
	}}
stage('mutation tests'){
steps{
sh 'mvn org.pitest:pitest-maven:mutationCoverage' 

}
Post{
//welke stappen moeten gebeuren na de stages (vaak stappen mbt reporting)
}
}


