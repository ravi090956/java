pipeline {
    agent none
options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '5')
}
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('read Read.me') {
            when {
                  branch 'dev'
                }
            steps {
                sh 'cat README.md'
            }
        }
    }
}
