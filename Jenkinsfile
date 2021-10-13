pipeline{
    agent{label 'master'}
        tools{maven 'M3'}
        stages{
            stage('Checkout'){
                steps{
                    git branch: 'main', url: 'https://github.com/mustakimdurvesh/SpringPetClinic.git'
                }
            }
            stage('Complie'){
                steps{
                    sh 'mvn compile'
                }
            }
             stage('Test'){
                steps{
                    sh 'mvn test'
                }
            }
             stage('Package'){
                steps{
                    sh 'mvn package'
                }
            }
            stage('Deploy'){
                steps{
                    
                    sh 'java -jar /var/lib/jenkins/workspace/PetClinicDelcarativePipeline/target/*.jar'
                }
            }
        }
    }
