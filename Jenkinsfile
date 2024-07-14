pipeline {
    agent any
    stages {
        stage("Prepare files") {
            steps {
                git branch: 'main', url: 'https://github.com/RedRatInTheHat/vector-role.git'
            }
        }
        stage("Build") {
            steps {
                sh 'python3 -m molecule test'
            }
        }
    }
}