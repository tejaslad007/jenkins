pipeline {
    agent any

    stages {
        stage('Hello') {
            agent {
                label "master"
            }
            steps {
                echo 'Hello World'
            }
        }
        stage('Hello2')
        {
            agent {
                label "Slave_Linux_Node"
            }
            steps {
                echo 'Hellow World 2'
            }
        }
        stage('Hello3')
        {
            agent{
                label "master"
            }
            steps{
                echo 'Hello World 3'
            }
        }
        stage('Run Parallel')
        {
            
            parallel {
                stage('Windows')
                { 
                    agent {
                label "Slave_Linux_Node"
            }
                    steps{
                        echo "Hello Windows"
                    }
                }
                stage('Linux')
                {
                    agent{
                        label "master"
                    }
                    steps{
                        echo "Hello Linux"
                    }
                    
                }
            }
        }
    }
}
