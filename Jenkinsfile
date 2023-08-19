pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'GitCred', url: 'https://github.com/MANSOORONE/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
     ansiblePlaybook credentialsId: 'Ansible', disableHostKeyChecking: true, inventory: 'dhost.inv', playbook: 'apache.yml'
      }
    }
}
}
