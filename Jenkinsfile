node {
  stage("Récupération des sources") {
    checkout scm
  }

  stage("Deploiement de l'application Back") {
    sh "echo APPLICATION-BACK"
  }
  echo "La branche ${env.BRANCH_NAME} a été déployé"
}