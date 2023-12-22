pipeline {
     agent {
        label 'agent1'
    }
 // using the Timestamper plugin we can add timestamps to the console log
    options {
        timestamps()
    }
    
    stages {
        stage('Write node name') {
            steps {
                echo "NODE_NAME = ${env.node_name}"
            }
        }
          
        stage('build') {
            steps {
                echo "Build step."
            }
        }
    
 
        stage('test') {
            steps {
                echo "Test stage."
            }
        }
    

        stage('deploy') {
            steps {
                echo "Deploy stage"
            }
        }
    }
    
    post {
        success {
                echo "Pipeline is succesfull."
        }
        failure {
                echo "Pipeline failed."
        }
        unstable {
                echo "Pipeline is unstable. Has some warnings etc."
        }
        cleanup {
                echo "Performed cleanup."
        }
    }
}