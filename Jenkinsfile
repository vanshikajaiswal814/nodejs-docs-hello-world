node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarQube';
    withSonarQubeEnv(credentialsId: 'sonarhii',installationName: 'sonar') {
      sh "${scannerHome}/sonar-scanner"
    }
  }
}
