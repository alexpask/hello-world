pipeline {
  agent {
    docker {
      image 'maven'
    }
    
  }
  stages {
    stage('Compile') {
      steps {
        sh 'mvn -B clean package'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }
  }
}