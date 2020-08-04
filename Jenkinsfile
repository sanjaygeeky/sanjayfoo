pipeline {
  agent {
    docker {
      image 'maven:3-openjdk-11'
    }

  }
  stages {
    stage('one') {
      steps {
        echo 'this is the first job'
        sh 'mvn compile'
      }
    }

    stage('two') {
      steps {
        echo 'this is the second job'
        sh 'mvn clean test'
      }
    }

    stage('three') {
      steps {
        echo 'this is the third job'
        sh 'mvn package -Dskiptests'
      }
    }

  }
  tools {
    maven 'Maven3.6.3'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}