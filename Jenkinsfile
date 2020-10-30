pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/targets/*.war', fingerprint: true)
        sh '''mkdir /home/sujit/buildoutput/${BUILD_NUMBER}
cp **/target/*.war /home/sujit/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}