pipeline{

    agent any

    stages {

        stage("build") {

            steps {
            sh 'npm i'
            sh 'npm run build'
            }

        }


        stage("Deploy") {

            steps {
            sh " ansible-playbook playbooks/node-app-deploy.yml --key-file '/var/lib/jenkins/id_rsa' " 
	

            }

        }

    }

}
