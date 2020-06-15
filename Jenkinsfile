node('master'){
   checkout scm
   stage('Build For Production'){
      withMaven(maven: 'M3')
      if(isUnix()){
          sh 'mvn -Dmaven.test.failure.ignore clean package'
      }
   }
}
