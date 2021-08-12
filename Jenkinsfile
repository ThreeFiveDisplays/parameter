
node('docker && android-build') { 
checkout scm


    parameters {
       string(name: 'hostname', defaultValue: 'gabor-dev', description: 'Hostname or IP address')
       booleanParam(name: 'yesno', defaultValue: false, description: 'Checkbox')
       choice(name: 'planet', choices: ['Mercury', 'Venus', 'Earth', 'Mars'], description:  'Pick a planet')
       choice(name: 'space', choices: ['', 'Mercury', 'Venus', 'Earth', 'Mars'], description:  'Pick a planet. Defaults to empty string')
       text(name: 'story', defaultValue: 'One\nTwo\nThree\n', description: '')
       password(name: 'secret', defaultValue: '', description: 'Type some secret')
       string(defaultValue: '1.0', description: 'Current version number', name: 'VERSION')
       booleanParam(defaultValue: false, description: 'If build should be marked as pre-release', name: 'PRERELEASE')
       string(defaultValue: 'ayufan-pine64', description: 'GitHub username or organization', name: 'GITHUB_USER')
       string(defaultValue: 'android-7.1', description: 'GitHub repository', name: 'GITHUB_REPO')
       booleanParam(defaultValue: true, description: 'Select if you want to build tablet version.', name: 'BUILD_TABLET')
       booleanParam(defaultValue: true, description: 'Select if you want to build TV version.', name: 'BUILD_TV')
       booleanParam(defaultValue: true, description: 'Select if you want to build Pinebook version.', name: 'BUILD_PINEBOOK')
 
    }
    stages {
        stage('display') {
            steps {
                echo params.hostname
                echo params.yesno ? "yes" : "no"
                echo params.planet
                echo params.space
                echo params.story
                //echo params.secret
                echo "--------"
                echo "${params.hostname}"
                echo "${params.yesno}"
                echo "${params.planet}"
                echo "${params.space}"
                echo "${params.story}"
                echo "${params.secret}"
                script {
                    sh "echo ${params.secret}"
                }
            }
        }
}
}

