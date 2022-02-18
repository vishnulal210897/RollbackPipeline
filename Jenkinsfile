pipeline {
     agent any
stages {
    stage('Copy Artifact') {
        steps {
            //copyArtifacts filter: '**', fingerprintArtifacts: true, projectName: 'cicd', selector: specific('$build_number')
             copyArtifacts fingerprintArtifacts: true, projectName: 'Stage Deployment', selector: lastSuccessful()
        }
    }
    stage('deploy the code on server'){
        steps{
            sh 'rm -r /var/www/html/sample/*'
            sh 'cp * /var/www/html/sample/'
            sh 'rm /var/www/html/sample/Jenkinsfile'
        }
    }
}
}
