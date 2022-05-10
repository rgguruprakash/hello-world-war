pipeline {
      agent none
      stages {
        stage('build') {
              agent { label 'slave-java' }
          steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                sh 'echo "STAGE 1 this is build stage"'
                       }
                }
        }    
    }
}

