pipeline {
    
    stages {
        stage('Example Build') {
      
            steps {
                echo 'Hello, Maven'
                sh 'mvn --version'
            }
        }
        stage('Example Test') {
           
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'git@github.com:SheikHussain/PipelineJ.git']]])
                sh 'java -version'
            }
        }
    }
}
