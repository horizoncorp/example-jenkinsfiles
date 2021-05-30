pipeline {
    agent any
    stages {
        stage('Validate jenkinsfile') {
            steps {
                script {
                    sh 'curl --user admin:admin -X POST -F "jenkinsfile=<parameterized/Jenkinsfile" ${JENKINS_URL}/pipeline-model-converter/validate'
                    sh 'curl --user admin:admin -X POST -F "jenkinsfile=<docker-agent/Jenkinsfile" ${JENKINS_URL}/pipeline-model-converter/validate'
                    sh 'curl --user admin:admin -X POST -F "jenkinsfile=<aws-authentication/Jenkinsfile.1" ${JENKINS_URL}/pipeline-model-converter/validate'
                    sh 'curl --user admin:admin -X POST -F "jenkinsfile=<aws-authentication/Jenkinsfile.2" ${JENKINS_URL}/pipeline-model-converter/validate'
                }
            }
        }
    }
}
