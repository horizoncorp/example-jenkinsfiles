pipeline {
    agent any
    stages {
        stage('Validate jenkinsfile') {
            steps {
                script {
                    sh 'curl --user admin:admin -X POST -F "jenkinsfile=<parameterized/Jenkinsfile" ${JENKINS_URL}/pipeline-model-converter/validate'
                }
            }
        }
    }
}
