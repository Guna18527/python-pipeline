pipeline {
    agent any
    
    stages {
        stage ('git checkout') {
            
            steps {
                git 'https://github.com/Guna18527/python-pipeline.git'
            }
        }
        
	 stage('Test') {
            steps {
                sh 'test'
            }
        }
    }

     post {
        always {
            echo 'post build action'
            build job: 'python'
            build job: 'maven project'
        }
    }

}
