pipeline {
    agent any

 parameters {
        string(name: 'fullname', defaultValue: 'eswar', description: 'Who should I say hello ?')
  }
  
    stages {
        stage('Hello') {
            steps {
                 echo "Hello ${params.fullname}"
            }
        }
         stage('myname') {
            steps {
                 echo "welcome to jenkins  ${params.fullname}"
            }
        }
    }
 post{
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
 }
     
}
