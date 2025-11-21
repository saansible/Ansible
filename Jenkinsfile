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
                    url: 'git@github.com:your-org/your-ansible-repo.git'
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
