pipeline {
    agent any
    
    tools {
        //install the maven version configured as "M3" and add it to the path.
        maven "M3"
    }
    
    stages {
        stage('Checkout') {
            steps {
                //get some code from a github repo
            git branch: 'main', url: 'https://github.com/DanicafDavies/lbg-hello-world-maven'
            }
        }
        stage('Compile') {
            steps {
                //Run Maven On A Unix Agent.
                sh "mvn clean compile"
            }
        }
         stage('Test') 
         {
            steps 
            {
                sh "mvn test"
            }
         }
        stage('Package') 
         {
            steps 
            {
                sh "mvn -Dmaven.test.skip package"
            }
        }      
    }
}
