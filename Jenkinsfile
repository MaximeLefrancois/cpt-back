
properties([
   parameters([
      string($class: 'StringParameterDefinition', defaultValue: 'horsprod', description: 'Quel environnement de deploiement ("prod" ou "horsprod")?', name: 'ENV_BACK'),
	  string($class: 'StringParameterDefinition', defaultValue: '', description: 'Identifiant compte AD', name: 'LOGIN'),
	  password($class: 'PasswordParameterDefinition', defaultValue: '', description: 'Password compte AD', name: 'PWD')
   ])
])

node {
	sh "echo le login est :${LOGIN} et le mot de passe est ${PWD}. "
	
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