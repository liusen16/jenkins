pipeline{
    agent any
    stages {
  stage('retrive and build') {
    steps {
      echo "retrive"
      git branch: 'main', credentialsId: '92b4713a-1ef8-4275-8a48-72f8804a89c4', url: 'ssh://git@ssh.github.com:443/liusen16/jenkins-maven'
      echo "build"
      withMaven(globalMavenSettingsConfig: '', jdk: '', maven: '', mavenSettingsConfig: '', traceability: true) {
      sh " mvn clean install"
      }
    }
  }
}
}
