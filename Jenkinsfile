pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t manikantapaila/new:train .'
            }
        }
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name train -p 9999:80 manikantapaila/new:train'
            }
        }
    }
}
