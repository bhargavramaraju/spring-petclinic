pipeline {
    agent any
    stages {
        stage ('git') {
            steps {
                git url: 'https://github.com/bhargavramaraju/spring-petclinic.git',
                    branch: 'main'
            }
        }
    }   
}
