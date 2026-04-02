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
                echo "Stopping current instance ..."
                sh "make stop"
            }
        }

        stage("Starting new instance") {
            steps {
                echo "Starting new instance ..."
                sh "make start"
            }
        }
    }
}