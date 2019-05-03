pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''gradlew assembleDebug
'''
      }
    }
    stage('save apk') {
      steps {
        archiveArtifacts(artifacts: '*.apk', onlyIfSuccessful: true)
      }
    }
  }
}