
properties([
   parameters([
      string(defaultValue: 'horsprod', description: 'Quel environnement de deploiement ("prod" ou "horsprod")?', name: 'ENV_BACK'),
	  string(defaultValue: '', description: 'Votre identifiant ?', name: 'LOGIN'),
	  password(defaultValue: '', description: 'Votre mot de passe ?', name: 'PWD')
   ])
])

node {
	
	stage("Récupération des sources") {
		checkout scm
	}

	stage("Deploiement de l'application Back") {
		sh "echo APPLICATION-BACK"
	}
	
	if (params.ENV_BACK == 'prod') {
		stage("Deploiement de l'application Back en prod") {
			sh "echo APPLICATION-BACK"
		}
	}
	echo "La release ${env.BRANCH_NAME} a été déployé sur l'environnement ${params.ENV_BACK}"
}