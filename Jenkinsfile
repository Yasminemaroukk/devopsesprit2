
pipeline {
    agent any
    triggers {
        // Configuration du déclenchement du pipeline lorsqu'un push est détecté dans le référentiel Git
        pollSCM 'H/5 * * * *'
    }
        stages {
        stage('Récupération du code source') {
            steps {
                git remote 'https://github.com/Yasminemaroukk/devopsesprit2.git'
            }
        } 
        stage('Affichage de la date système') {
            steps {
                // Cette étape affiche la date système
                script {
                    def date = sh(script: 'date', returnStdout: true).trim()
                    echo "La date système est : ${date}"

                }

            }

        }

    }

}
