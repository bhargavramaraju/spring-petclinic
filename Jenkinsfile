pipeline {
    agent any
    stages {
        stage('Git') {
            steps {
                git url: 'https://github.com/bhargavramaraju/spring-petclinic.git',
                   branch: 'main'
            }
        }
        stage('k8s') {
            steps {
                withKubeConfig([credentialsId: 'k8', serverUrl: '']) {
                    sh 'kubectl apply -f deployment.yaml'
                }
            }
        }
    }
}
