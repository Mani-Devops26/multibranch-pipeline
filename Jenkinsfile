pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t manikantapaila/new:bus .'
            }
        }
        
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bus -p 8888:80 manikantapaila/new:bus'
            }
        }
    }
}
