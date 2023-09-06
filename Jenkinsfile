node {
  stage('SCM') {
    git 'https://github.com/zouyingjie/spring-restdocs'
  }

    stage('SonarQube analysis') {
    withSonarQubeEnv() { // Will pick the global server connection you have configured
      sh './gradlew sonarqube'
    }
  }
}
