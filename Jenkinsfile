node {
  
  stage("ENV Test") {
	  echo "test use"
  }

  stage("Test 2") {
	  echo "test use"
  }

  stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
	
}
