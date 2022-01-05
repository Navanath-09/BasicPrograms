pipeline {
    agent {
	       label {
                label "node2"		   
	
	}
	}
    stages {
        stage('Httpd_installation') {
            steps {
                sh "sudo yum install httpd -y"
            }
        }
    
       stage('start_service') {
            steps {
                sh "sudo service httpd start"
            }
        }
        stage('status_check') {
            steps {
                sh "sudo service httpd status"
            }
        }
		stage('deploy_on_server') {
            steps {
               sh "echo '2nd time change hello navanath successfully deploy on server' >> index.html"
               sh "sudo cp -r index.html /var/www/html/"
			
            }
        }
    }
}
