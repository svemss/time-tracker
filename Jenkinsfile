pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "hi"
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
