pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh 'cd /root/cicd-pipeline-train-schedule-jenkins'
                sh 'sudo ./gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
                sh 'sudo ./gradlew npm_start'
            }
        }
    }
}
