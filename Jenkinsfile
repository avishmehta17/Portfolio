pipeline {
    agent {label "popat"}

    stages {
        stage('Clone') {
            steps {
                echo "cloning the code"
                git url:"https://github.com/avishmehta17/Portfolio.git", branch: "main"
            }
        }
        stage('Build') {
            steps {
                sh "docker build -t myimage ."
            }
        }
        stage('Deploy') {
            steps {
                sh "docker compose up -d"
            }
        }
    }
}
