pipeline {
    agent any
    stages {
        tools {
      maven "M3"
               }
        
        stage('Build Application') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true clean package'
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
