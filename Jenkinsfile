pipeline {
    agent any

    stages {
        stage("Clone project") {
            steps {
                echo "Cloning project ..."

                git branch: "main", url: 'git@github.com:Oualitsen/grafana.git'
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