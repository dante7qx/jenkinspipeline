pipeline {
    agent any
    stages {
       stage('build') {
          steps {
             sh 'echo step1'
             sh 'echo step2'
             sh '''
                echo 'Multiline'
                echo 'Example'
             '''
             echo 'not using shell'
          }
       }
       stage('测试') {
	   steps {
             sh "echo Test"
           }
           stage('ie') {
               steps {
	           sh "ie test..."
               }
           }
       }
       stage('deploy') {
           steps {
               sh "mvn -v"
           }
       }
    }
}
