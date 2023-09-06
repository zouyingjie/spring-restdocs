node {
  stage('SCM') {
    git 'https://github.com/zouyingjie/spring-restdocs'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv(installationName: 'sonarqube-server-for-ci') { // You can override the credential to be used
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
    }
  }
}
