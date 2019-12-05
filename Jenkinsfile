pipeline{
	agent any //update to reflect environment
		
		stages{
			stage('Preparing environment'){
				steps{
				cleanWs() //requires workspace clean up plugin
				//add environment variables
			}
		}
			stage('Code checkout'){
				steps{
				checkout scm 
				}
			}
<<<<<<< HEAD
		
/*		stage('Terraform init'){
				steps{
					sh 'terraform init -input=false'
					}
				}
=======
//			stage('Terraform init'){
//				steps{
//					sh 'terraform init -input=false'
//					}
//				}
>>>>>>> 07f81876949632e6e14e4c348f1d97ec2c51c554
			
//			stage('Run tests'){
//				steps{
//				if (fileExists('plan.out')){
//					echo 'Terraform plan exists already!'
//				}
//				else{
//					echo 'Terraform plan does not exist. Creating...'
//					sh 'terraform plan -out=plan.out -input=false'
//					if (fileExists('plan.out')){
//						echo 'Terraform plan has been created.'
//					}
//					else{
//						echo 'Terraform plan has not been created. Aborting...'
//						currentBuild.result = 'ABORTED'
//					}
//				}
//				sh 'terraform-compliance -p plan.out -f /path/to/srcipts'
//				}
//			}
//			stage('Approve the plan'){
//				steps{
//				input 'Approve the Terraform plan and proceed to deployment?'
//				}
//			}
			
<<<<<<< HEAD
			stage('Deploying the configuration'){
				steps{
				sh 'terraform apply -input=false plan.out'
				}
			}
*/				
=======
//			stage('Deploying the configuration'){
//				steps{
//				sh 'terraform apply -input=false plan.out'
//				}
//			}	
>>>>>>> 07f81876949632e6e14e4c348f1d97ec2c51c554
			stage('Code check'){
				steps{
					//insert code checks
					}
			}
			
			stage('Build the app'){
				steps{
				script {
                  def pom = readMavenPom file: 'pom.xml'
                  version = pom.version
              }
					sh "mvn clean install -DskipTests=true"
				}
			}
			
			stage('Test'){
				steps{
					//insert functional/integration tests
				}
			}
			
			stage('Archive'){
				steps{
					//insert artifact repository
				}
			}
			
			stage('Deploy'){
				steps{
					sh "mvn clean package"
				}
			}
		}
<<<<<<< HEAD
	}
=======
	}
>>>>>>> 07f81876949632e6e14e4c348f1d97ec2c51c554
