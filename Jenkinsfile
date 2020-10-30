pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war', fingerprint: true)
        sh '''mkdir /home/sujit/buildoutput/${BUILD_NUMBER}
cp /var/lib/jenkins/workspace/javademos_master/javademos-master/ssgsems/target/*.war /home/sujit/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}