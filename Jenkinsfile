pipeline{
  agent any  
  stages{  
      stage("Run ansible playbook"){
        steps{
        ansiblePlaybook credentialsId: 'ssh-key', inventory: 'hosts', playbook: 'nginx_install.yaml', vaultTmpPath: ''
        }
      }
    stage('print nginx is Installed') {
      steps{
         sh"echo nginx is installed on all servers"
        
      }
      
    }
  }
}
