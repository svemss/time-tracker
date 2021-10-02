pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "hi"
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
        stage('deploy') {
            steps {
                deploy adapters: [tomcat9(credentialsId: 'tomcat-manager-scripts', path: '', url: 'http://localhost:9080')], contextPath: '/demo', war: '**/*.war'
            }
        }
    }
}
