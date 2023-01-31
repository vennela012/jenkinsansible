pipeline{
    agent { label ' NODE1'}
    stages {
        stage('vcs') {
            steps {
                git url: 'https://github.com/vennela012/ansiblejenkins.git',
                branch: 'main'
                }
            }
            stage('installing apache2 using playbook') {
                steps {
                    sh 'ansible-playbook -i hosts apache2.yaml'
                }
            }
    }
}