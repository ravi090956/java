pipeline {
    agent any
options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10')
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
        stage('target environment') {
            parallel {
                stage('info') {
                    steps {
                        echo 'info'
                    }
                }
                stage('copy') {
                    steps {
                        echo 'copy'
                    }
                }
                stage('publish') {
                    steps {
                        echo 'publish'
                    }
                }
            }
        }
    }
}
