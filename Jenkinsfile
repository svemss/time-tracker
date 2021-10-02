pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "hi"
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        stage('deploy') {
            steps {
                echo "hi"
                url "http://localhost:9080"
                war "**/*.war"
                contextpath "/demo"
            }
        }
    }
}
