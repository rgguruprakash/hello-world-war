pipeline {
      agent { label 'slave-java' }
      stages {
        stage('build') {
          steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                sh 'echo "STAGE 1 this is build stage"'
                       }
                }
        }
           stage('Test and Deploy') { 
				
				parallel {
					stage('Test') { 
						steps {
							sh '''
								   echo "$NODE_NAME -> $JOB_NAME -> $BUILD_NUMBER "
								   sleep 5
							   ''' 
						}
					}
					
					stage('Deploy') { 
						steps {
							sh ''' 
								mvn clean install
							   '''
                                    }
                              }
                        }
           }
      }
}
                                          
          
                 
                  
                  
                  
                  
				

