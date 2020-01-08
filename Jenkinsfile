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
		success { 
			sendNotificationToCDD appName: 'CDD-Training-DEV', 
					appVersion:  "${env.BRANCH_NAME}", 
					gitCommit: 'AAAA',
					gitPrevSuccessfulCommit: 'Assaf',
					overrideCDDConfig: [
							customApiKey: 'eyJhbGciOiJIUzUxMiJ9.eyJ1c2VybmFtZSI6InN1cGVydXNlckBjYS5jb20iLCJ0ZW5hbnRJZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDAwMDAwMDAwMCIsImVtYWlsIjpudWxsLCJmaXJzdE5hbWUiOm51bGwsImxhc3ROYW1lIjpudWxsLCJyb2xlcyI6bnVsbCwidXNlcklkIjoxLCJqdGkiOiI1NDA5MzM2Yi05NTNjLTRlMDAtYjMxNC0zODUxZmQ5ZjRjMmYiLCJleHAiOjE1NTk0Nzc5NjR9.hFRz6l1lwdj15_PxHi5IT2YmxZ6p3Kchw_zn1y4UAuruICn7jhwvvu0tKT7TfdsDUw9DtLbCoVV5MJ1fp7ez-g',
							customProxyPassword: '',
                            				customProxyUrl: '',
                            				customProxyUsername: '',
                            				customServerName: 'http://lvntest002908.bpc.broadcom.net',
                            				customServerPort: 8080,
                            				customTenantId: '00000000-0000-0000-0000-000000000000',
                            				customUseSSL: false
                    ],
					releaseTokens: '{}'
		}
	}
}
