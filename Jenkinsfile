pipeline {
     agent any

stages {
    stage('Copy Artifact') {
        steps {
            //copyArtifacts filter: '**', fingerprintArtifacts: true, projectName: 'cicd', selector: specific('$build_number')
             copyArtifacts fingerprintArtifacts: true, projectName: 'Stage Deployment', selector: lastSuccessful()
        }
    }
    //stage('deploy the code on server'){
      //  steps{
        //    sshPublisher(publishers: [sshPublisherDesc(configName: 'stage', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'var/www/rollback-demo/' , remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/*')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
        //}
    //}
}
}
