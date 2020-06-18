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
                sh label: '', script: 'rsync -o stricthostkeychecking=no target/* root@13.57.234.158:/home/phpbuild/'
            }
        }
    }
 }
