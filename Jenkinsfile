pipeline {
    agent any
    stages {
       stage("SCM Checkout") {
          steps {
              git credentialsId: 'github', url: 'https://github.com/gauravlohani/ansible-roles.git'
                }
        }
    }
 }
