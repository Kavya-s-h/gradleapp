pipeline{
 agent any //use any avilable agent
 tools{
 	gradle 'Gradle'
 	jdk 'JDK'
 	}
 stages{
 stage('Checkout'){
 	steps{
 	git branch:'main',url:'https://github.com/Kavya-s-h/My-Gradle-App.git'
 	}
 	}
 	
 	stage('Build'){
 		steps{
 		sh'gradle build'
 		}
 	}
 	
 	stage('Test'){
 	steps{
 	 sh 'gradle test'
 	 }
 	} 
 	
 	stage('Run Application'){
 		steps{
 		// start
 		sh 'gradle run'
 		}
 	}	
 }
 
 post{
 	success{
 	echo'Build and deployement successful!'
 	}
 	failure{
 	echo 'Build failed!'
 	}
