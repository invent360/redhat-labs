pipeline {
    agent any
    options {
      timeout(time: 20, unit: 'MINUTES') 
    }
    stages {
      stage('preamble') {
          node("maven") {
            sh "git clone https://github.com/openshift/openshift-jee-sample.git ."
            sh "mvn -B -Popenshift package"
          }
          // steps {
          //   sh "echo $PATH"
          // }
      }
  }
}