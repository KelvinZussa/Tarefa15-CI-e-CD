pipeline {
    agent any

    stages {
        stage('setup') {
            steps {
                git branch: 'main', url: 'https://github.com/KelvinZussa/Tarefa15-CI-e-CD.git'
                bat 'npm install'
            }
        }

        stage('Inciar Serverest') {
            steps {
                bat '''set NO_COLOR=1
                npm start'''
            }
        }

        stage('Inciar Teste') {
            steps {
                bat '''set NO_COLOR=1
                npm run cy:run'''
            }
        }
    }
}
