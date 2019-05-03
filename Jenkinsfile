pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''chmod +x gradlew
./gradlew assembleDebug
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