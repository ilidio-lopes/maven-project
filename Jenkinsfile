pipeline {
    agent any
    stages {
        stage("Init") {
            steps {
                bat "mvn clean package"
            }
            post {
                success {
                    echo "Now archiving..."
                    archiveArtifacts artifacts: "**/*.war"
                }
            }
        }
    }
}