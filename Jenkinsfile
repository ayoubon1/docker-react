pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build') {
      steps {
        script {
          // Installation des dépendances Node.js
          nodejs(nodeJSInstallationName: 'YourNodeJSInstallation') {
            sh 'npm install'
          }

          // Build de l'application React
          sh 'npm run build'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          // Exécuter les tests, si nécessaire
          sh 'npm test'
        }
      }
    }

    stage('Deploy') {
      steps {
        // Déployer l'application, par exemple sur un serveur web
        // Vous pouvez utiliser ssh, scp, ou d'autres moyens selon votre environnement
      }
    }
  }
}
