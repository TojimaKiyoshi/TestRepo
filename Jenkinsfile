pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''export ANDROID_HOME=/usr/local/android-sdk/
chmod +x gradlew
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