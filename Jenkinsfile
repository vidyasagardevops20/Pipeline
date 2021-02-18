pipeline {
	agent {
		label 'MasterGroup'
	}
	triggers {
		pollSCM '* * * * *'
	}
	stages {
		stage ("Clone GOL - GitHub Central Repo") {
			steps {
				git 'https://github.com/wakaleo/game-of-life.git'
			}
		}
		stage ("Build GOL - MAVEN") {
			steps {
				sh 'mvn clean package'
			}
		}
		stage ("Archive Artifacts") {
			steps {
				archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
			}
		}
		stage ("Publish Junit Test Results") {
			steps {
				junit 'gameoflife-web/target/surefire-reports/*.xml'
			}
		}
	}
}
