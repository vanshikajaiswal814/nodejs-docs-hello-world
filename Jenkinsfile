node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarQube';
    withSonarQubeEnv('sonar') {
      sh "${scannerHome}/sonar-scanner"
    }
  }
}
