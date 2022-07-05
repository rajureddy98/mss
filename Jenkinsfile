pipeline {
    agent any
 
    stages {
        stage('clean WS') {
            steps {
                cleanWs()
            }
        }
        stage('scm checkout') {
            steps {
               git 'https://github.com/rajureddy98/mss.git' 
            }
        }
        stage('parent-build'){
            steps {
                sh '''
                    echo $JAVA_HOME
                    mvn clean package
                '''
            }
        }
    }
}
