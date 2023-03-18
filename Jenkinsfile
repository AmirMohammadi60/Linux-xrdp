pipeline {
  agent any
  
  stages {
    stage('Install xrdp') {
      steps {
        sh 'echo "Amir1225601225" | sudo -S apt-get update'
        sh 'sudo -t apt-get install xrdp -y'
      }
    }
    
    stage('Configure xrdp') {
      steps {
        sh 'sudo sed -i \'s/allowed_users=console/allowed_users=anybody/g\' /etc/X11/Xwrapper.config'
        sh 'echo "xfce4-session" > ~/.xsession'
        sh 'sudo service xrdp restart'
      }
    }
  }
}
