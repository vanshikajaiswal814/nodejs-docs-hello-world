node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonar1';
    withSonarQubeEnv('sonar') {
      sh "${scannerHome}/sonar-scanner"
    }
  }
}
