pipeline {
    agent any
        tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "M3"
   }
    stages {            
        stage('Build Application') {
            steps {
                bat 'mvn -Dmaven.test.failure.ignore=true clean package'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }
        stage('Deploy in Staging Environment'){
            steps{
                echo "Start deploying into staging envi"
 
            }
            
        }
       
    }
}
