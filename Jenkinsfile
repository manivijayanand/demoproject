pipeline {
  agent {
    label 'maven'
  }
  tools{
    maven 'maven-3.6.2'
  }
  parameters{
    choice(choices: 'UNIT', description:'pipeline?', name: 'PIPELINE')
  }
  stages {
  stage('Build') {
      steps {
        script {
          echo 'Stage 1'
          rtMavenRun(
            tool:"maven-3.6.2",
            pom:"pom.xml",
            goals:"--batch-mode -V -U -e clean package -Dmaven.test.skip=true -Dsurefire.useFile=false",
            resolverId:"MAVEN_RESOLVER"
            )
        }
      }
    }
    
  stage('Stage 2') {
      steps {
        script {
          echo 'Stage 2'
        }
      }
    }
  }
}
