pipeline {

    agent {
        node {
            label 'mac'
        }
    }
    stages {
        stage('Docker') {
            steps {
                withDocker('hmcts/moj-gatling-image', null) {
                    sh 'ls -l /etc/gatling/conf'
                }
            }
        }
    }
}