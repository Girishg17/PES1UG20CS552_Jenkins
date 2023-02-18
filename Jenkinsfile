pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o finaloutput a2.cpp'
            }
        }
        stage('Test') { 
            steps {
                sh './finaloutput'
                
            }
        }
        stage('Deploy') { 
            steps {
                // sh 'cat a2.cpp'
                error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}