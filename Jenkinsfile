
pipeline {

    agent { label 'master' }
    parameters {
       string(defaultValue: '1.0', description: 'Current version number', name: 'VERSION')
       booleanParam(defaultValue: false, description: 'If build should be marked as pre-release', name: 'PRERELEASE')
       string(defaultValue: 'ayufan-pine64', description: 'GitHub username or organization', name: 'GITHUB_USER')
       string(defaultValue: 'android-7.1', description: 'GitHub repository', name: 'GITHUB_REPO')
       booleanParam(defaultValue: true, description: 'Select if you want to build tablet version.', name: 'BUILD_TABLET')
       booleanParam(defaultValue: false, description: 'Select if you want to build TV version.', name: 'BUILD_TV')
       booleanParam(defaultValue: false, description: 'Select if you want to build Pinebook version.', name: 'BUILD_PINEBOOK')
 
    }
    stages {
        stage('display') {
            steps {
                echo "Bill"
            }
        }
}
}

node('docker && android-build') { 

}
