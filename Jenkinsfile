pipeline {
    agent any
    stages {
        stage("verfiy tooling") {
            steps {
                sh '''
                    docker version
                    docker info
                    docker compose version
                    curl --version
                    jq --version
                '''
            }
        }
    }
}