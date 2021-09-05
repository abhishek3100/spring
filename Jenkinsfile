pipeline {
    agent any 
    stages {

        stage('Cooking') {
            steps {
                // Clean before build
                cleanWs()
                // We need to explicitly checkout from SCM here
                checkout scm
                echo "Building ${env.JOB_NAME}..."
            }
        }
        
        stage('Build') { 
            steps {
                sh ''' 
                    echo "this is build stage....."
                    sleep 10
                '''
            }
        }
        stage('Test') { 
            steps {
                sh ''' 
                    echo "this is test stage......"
                    sleep 10
                ''' 
            }
        }
        stage('Deploy') { 
            steps {
                sh ''' 
                    echo "this is deploy stage....."
                    sleep 10
                '''
            }
        }

        stage('Running File') {
            steps {
                sh ''' 
                echo "Running file from Fol1 in 5 sec..."
                chown -R $USER:$USER ./fol1/hello.sh
                chmod +x ./fol1/hello.sh
                sleep 5
                ./fol1/hello.sh 
                
                '''
            }
        }
    }
}