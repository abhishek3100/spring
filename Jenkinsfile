pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh ''' 
                    echo "this is build stage.....
                    sleep 10
                '''
            }
        }
        stage('Test') { 
            steps {
                sh ''' 
                    echo "this is test stage......
                    sleep 10
                ''' 
            }
        }
        stage('Deploy') { 
            steps {
                sh ''' 
                    echo "this is deploy stage.....
                    sleep 10
                '''
            }
        }

        stage('Running File') {
            steps {
                sh ''' 
                echo "Running file from Fol1 in 5 sec..."
                sleep 5
                ./fol1/hello.sh '''
            }
        }
    }
}