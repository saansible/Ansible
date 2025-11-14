pipeline {
    agent sa_ansible

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i hosts uptime.yml'
            }
        }
    }
}
