pipeline {
    agent any
   
    stages {
        stage('Starting') {
            steps {
                echo 'Started pipeline'
            }
        }
        
        // stage('setup'){
        //     steps{
        //         bat 'mvn clean'
        //     }
        // }
        // stage('test'){
        //     steps{
        //         bat 'mvn test'
        //     }
        // }
        stage('Building'){
        triggers{
            pollSCM('* * * * *')        
        }
        
            steps{
                
                bat 'mvn clean install -Dmaven.test.skip=true'
            }
        }
    }
}
