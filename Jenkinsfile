pipeline {
	agent none
	stages {
		stage("Name : Stage 1") {
			agent {
				label 'Group1'
			}
			steps {
				echo "Welcome to Genesso Trainings"
			}
		}
		stage("Name : Stage 2") {
			agent {
				label 'Group1'
			}
			steps {
				echo "This is the second stage of Declarative Pipeline"
			}
		}
		stage("Hyderabad") {
			agent {
				label 'MasterGroup'
			}
			steps {
				echo "This stage is for Hyderabad"
			}
		}
	}
}
