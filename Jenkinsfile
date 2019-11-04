pipeline {
    agent { docker { image 'python:2.7.9' } }
    
    
    stages {
        stage ("clean"){
            steps {
                sh "rm -rf python-ip-script"
            }
        }
        stage('build'){
            steps {
                sh 'pip install requests'
            }    
        }
        stage ("git clone"){
            steps {
                sh "git clone https://github.com/beerkeeper/python-ip-script.git"
            }
        }
        stage ("run script"){
            steps {
                sh "python python-ip-script/main.py"
            }
        }

    }
}

