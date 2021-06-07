pipeline {
  agent any
  stages {
    stage('initialize') {
      steps {
        sh 'gradle run -Pinpath=$WORKSPACE/boulder_input -Poutpath=$WORKSPACE/content -Pconcurrent-uploads=4 -Pakamai-base-url-for-hnt=$AKAMAI_BASE_URL_FOR_HNT'
        warnError(message: 'boulder failed', catchInterruptions: true) {
          echo 'boulder failed'
        }

      }
    }

  }
}