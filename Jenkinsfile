pipeline {
	agent any
	
	stages {
		stage('1.checkout') { 
			steps { 
				// Checkout est implicite, on affiche un message
				echo "Code checked out succesfully." 
			} 
		}
		stage('2.Build') { 
			steps { 
				echo "Building the application..." 
				// Utilise le wrapper Maven pour la portabilité
				sh './mvnw compile'
			} 
		}
		stage('3.Test') {
			steps {
				echo "Running tests..."
				sh './mvnw test' 
			}
		}
	}
}


