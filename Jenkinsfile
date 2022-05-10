pipeline {
      agent any
      stages {
        stage('build') {
          steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                sh 'echo "STAGE 1 this is build stage"'
                       }
                }
        }    
    }
}

