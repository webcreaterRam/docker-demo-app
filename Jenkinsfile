pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/webcreaterRam/docker-demo-app.git'
            }
        }

        stage('Deploy via Ansible') {
            steps {
                sh 'ansible-playbook /etc/ansible/deploy.yml'
            }
        }
    }
}
