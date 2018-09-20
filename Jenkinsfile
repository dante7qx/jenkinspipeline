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
         parallel {
           stage('firefox') {
	       steps {
                   sh "echo firefox test..."
               }
           }
           stage('ie') {
               steps {
	           sh "echo ie test..."
               }
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
