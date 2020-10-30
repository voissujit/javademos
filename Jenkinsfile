pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
      }
    }

  }
}