pipeline {
    agent any
    stages {
        stage("Prepare files") {
            steps {
                dir ('vector-role') {
                    git branch: 'main', url: 'https://github.com/RedRatInTheHat/vector-role.git'
                }
            }
        }
        stage("Build") {
            steps {
                dir ('vector-role') {
                    sh 'python3 -m molecule test'
                }
            }
        }
    }
}