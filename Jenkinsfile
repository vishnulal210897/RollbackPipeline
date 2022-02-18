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
            sh 'rm -r *'
            sh 'cp -r . /var/www/html/sample/'
            sh 'rm Jenkinsfile'
        }
    }
}
}
