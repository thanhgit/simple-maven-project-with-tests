node('master') {
   checkout scm
   stage('Build') {
      withMaven(maven: 'M3')
      if (isUnix()) {
          sh 'mvn -Dmaven.test.failure.ignore clean package'
      }
   }

   stage('Test') {
      junit '**/target/surefire-reports/TEST-*.xml'
   }     
}
