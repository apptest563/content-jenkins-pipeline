pipeline {
  agent any    
  stages {
    stage('build') {
      steps {
        sh 'javac -d . src/*.java'
        sh 'echo Main-Class: Rectangulator > MAINFEST.MF'
        sh 'jar -cvmf MAINFEST.MF rectangle.jar *.class'
      }
    }
    stage('run') {
      steps {
         sh 'java -jar rectangle.java 10 80'
      }
    }
  }
}
