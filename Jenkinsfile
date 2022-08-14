pipeline {
    agent any

    stages {
       stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/gunjeet400/fizzbuzz.git']]])
            } 
       }
       stage('Build') {
            steps {
                git 'https://github.com/gunjeet400/fizzbuzz.git'
                bat 'python task0.py'
            } 
        }
    }
}
