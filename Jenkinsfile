pipeline {
    //Directives
    agent any
    tools {
        maven 'Maven'
    }

    stages {
        // Specify various stage with in stages

        // stage 1. Build project
        stage ('Build'){
            steps {
                sh 'mvn clean install package'
            }
        }

        // Stage2 : Testing
        stage ('Test'){
            steps {
                echo ' testing......'

            }
        }

       
        // Stage3 : Deploying
        stage ('Deploy'){
            steps {
                echo 'deploying......'
                }

            }
        }

        
        
    }
    


