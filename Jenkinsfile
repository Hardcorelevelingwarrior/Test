node{
    stage('SCM') {
        git branch: 'main', credentialsId: 'github-credentials', url: 'https://github.com/anhlahong/oopbee.git'}
    stage('SonarQube Analysis') {
        def scannerHome = tool 'SonarQube Scanner';withSonarQubeEnv() {sh  "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=.  -Dsonar.projectKey=test -Dsonar.login=squ_c9892daffbb2714637b9e093ecdbcc84648a16a6"}
        }
    }