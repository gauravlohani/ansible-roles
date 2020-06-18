pipeline {
    agent any
    stages {
       stage("SCM Checkout") {
          steps {
              git credentialsId: 'github', url: 'https://github.com/gauravlohani/ansible-roles.git'
                }
        }
        stage("Release build in production") {
            steps {
                sshagent(['ansibleserver']) {
                 sh label: '', script: 'scp -r /var/lib/jenkins/workspace/phpbuildfromgithub -o StrictHostKeyChecking=no root@13.57.234.158:/home/phpbuild/'
                 }
             }
        }
    }
 }
