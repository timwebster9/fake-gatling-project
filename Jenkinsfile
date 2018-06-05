pipeline {

    agent {
        node {
            label 'mac'
        }
    }
    stages {
        stage('Docker') {
            steps {
                withDocker('hmcts/moj-gatling-image', '-v $WORKSPACE/src/gatling/conf:/etc/gatling/conf') {
                    sh 'ls -l /etc/gatling/conf'
                }
            }
        }
    }
}