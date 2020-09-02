pipeline {
    agent any

    tools {
        maven 'localMaven'
    }

    stages{
        stage('Init'){
            steps {
                echo "Testing..."
            }
        }
        
        stage('Build'){
             steps {
                 echo 'Building...'
             }
        }
                
        stage ('Deploy'){
            steps {
                echo 'Code deployed.'
            }
        }
    }
}
