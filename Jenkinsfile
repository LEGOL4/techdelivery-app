pipeline {
    agent any

    stages {
        stage('Clonar') {
            steps {
                echo 'Clonando repositorio desde GitHub...'
            }
        }

        stage('Instalar dependencias') {
            steps {
                sh 'npm install'
            }
        }

        stage('Ejecutar pruebas') {
            steps {
                sh 'npm test'
            }
        }

        stage('Publicar aplicación') {
            steps {
                echo 'Aplicación lista para despliegue 🚚'
                sh 'node -e "console.log(require(\"./package.json\").version)"'
            }
        }
    }
}