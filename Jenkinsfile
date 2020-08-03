pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
   tools{
       maven 'Maven3.6.3' 
    }
  

    stages{
        stage('one'){
            steps{
                echo 'this is the first job'
                sh 'mvn compile'
               
            }
        }
        stage('two'){
            steps{
                echo 'this is the second job'
                sh 'mvn clean test'
                 }
        }
        stage('three'){
            steps{
                echo 'this is the third job'
                sh 'mvn package -Dskiptests'
                 }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}

