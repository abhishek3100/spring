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
            when {
                allOf {
                    branch 'main'
                    changeset 'fol1/**'
                }
            }
            steps {
                sh ''' 
                    echo "this is build stage....."
                    sleep 10
                '''
            }
        }
        stage('Test') { 
            when {
                allOf {
                    branch 'main'
                    changeset 'fol1/**'
                }
            }
            steps {
                sh ''' 
                    echo "this is test stage......"
                    sleep 10
                ''' 
            }
        }
        stage('Deploy') { 
            when {
                allOf {
                    branch 'main'
                    changeset 'fol1/**'
                }
            }
            steps {
                sh ''' 
                    echo "this is deploy stage....."
                    sleep 10
                '''
            }
        }

        stage('Running File') {
            when {
                allOf {
                    branch 'main'
                    changeset 'fol1/**'
                }
            }
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

