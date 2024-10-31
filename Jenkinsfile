pipeline {
    agent any
    stages {
        stage('Clonar Repositorio') {
            steps {
                git 'https://github.com/marisolcasilass/tu-repositorio.git'
            }
        }
        stage('Construir Imagen de Docker') {
            steps {
                script {
                    sh 'docker build -t mi_api_rest .'
                }
            }
        }
        stage('Ejecutar Pruebas') {
            steps {
                script {
                    sh 'docker run mi_api_rest pytest tests/' // Ajusta según tu estructura de pruebas
                }
            }
        }
    }
}
