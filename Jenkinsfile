pipeline {
    angent any

    stages {
        stage("Clone project") {
            steps {
                echo "Cloning project ..."

                git branch: "${params.BRANCH}",  url: 'git@github.com:retailapps/futuretail-switch-backend.git'
            }
        }

        stage("Stopping current instance") {
            steps {
                echo "Cloning project ..."  
                sh "make stop"
            }
        }

        stage("Starting new instance") {
            steps {
                echo "Cloning project ..."  
                sh "make start"
            }
        }
    }
}