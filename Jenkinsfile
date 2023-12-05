pipeline {
    agent any

    tools {
        nodejs 'NodeJsNPM'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Test') {
            steps {
                script {
                    // Instalar dependencias
                    sh 'npm install'
                    sh 'npm install --save-dev @testing-library/react-native@12.4.1 -force'
                    // Ejecutar pruebas
                    sh 'npm test'
                }
            }
        }
    }
}
