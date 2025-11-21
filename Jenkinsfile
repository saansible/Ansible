pipeline {
    agent any

    environment {
        // Path to your SSH key if needed for Ansible
        ANSIBLE_HOST_KEY_CHECKING = "False"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/saansible/Ansible.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh """
                    ansible-playbook -i hosts uptime.yml
                """
            }
        }
    }
}
