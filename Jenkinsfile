pipeline {
    //Directives
    agent any
    tools {
        maven 'maven'
    }

    stages {
        // Specify various stage with in stages

        // stage 1. Build
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

        //stage 3 publish the artifacts to nexus
        stage ("Publish to Nexus"){
            steps{
                nexusArtifactUploader artifacts: [[artifactId: 'VinayDevOpsLab', classifier: '', file: 'target/VinayDevOpsLab-0.0.4-jenkin.war', type: 'war']], credentialsId: 'd54fc65c-6fd2-4802-8df9-c0a62abe3683', groupId: 'com.vinaysdevopslab', nexusUrl: '172.20.10.20:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'Mylab-snapshot', version: '0.0.4-jenkin'
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

