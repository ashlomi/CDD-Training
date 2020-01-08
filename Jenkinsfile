pipeline {
    agent {
        label "master"
	}
    stages {
        stage("Export Porject") {
            steps {
             echo '**** mvn Build****'
			}
        }
        stage("Zip Project") {
            steps {
                echo '**** mvn Build****'    
            }
        }
        stage("Publish to Nexus") {
            steps {
			  echo "*** nexusVersion"       
			}
		}
	}		
    post { 
		always { 
			echo '----------Sending Build Notification to CDD--------------'
		}
		
					echo "${env.BRANCH_NAME}"
					echo "${env.GIT_COMMIT}"
					echo "${env.GIT_PREVIOUS_SUCCESSFUL_COMMIT}"
		}
}
