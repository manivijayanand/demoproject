pipeline {
  agent any
  parameters{
    choice(choices: 'UNIT', description:'pipeline?', name: 'PIPELINE')
  }
  stages {
  stage('Build') {
      steps {
        script {
          echo 'Build'
                          sh 'mvn -B --batch-mode -V -U -e clean package -Dmaven.test.skip=true -Dsurefire.useFile=false' 


        }
      }
    }
    
  stage('Stage 2') {
      steps {
        script {
          echo 'Stage 122'
        }
      }
    }
  }
}
