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
                bat 'npm install'
            }
        }

        stage('Ejecutar pruebas') {
            steps {
                bat 'npm test'
            }
        }

        stage('Publicar aplicacion') {
            steps {
                echo 'Aplicacion lista para despliegue'
                bat 'node -e "console.log(require(\"./package.json\").version)"'
            }
        }
    }
}