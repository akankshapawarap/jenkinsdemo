pipeline {
  agent any
  stages {
    stage('install apache') {
      steps {
        sh 'sudo service apache2 start'
      }
    }

    stage('checkout code') {
      steps {
        git(url: 'https://github.com/akankshapawarap/jenkinsdemo.git', branch: 'main')
      }
    }

    stage('deploy code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
        sh 'sudo service apache2 restart'
      }
    }

  }
}