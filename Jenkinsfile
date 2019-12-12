pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew -Dhttp.proxyHost=proxy -Dhttp.proxyPort=2011 -Dhttps.proxyHost=proxy -Dhttps.proxyPort=2011 build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
