pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                shell(script: "mv build.log ${flavor}-L1-docker.log || true")
                archiveArtifacts artifacts: "${flavor}-L1-docker.log", allowEmptyArchive: true
            }
        }
    }
}
