pipeline {
    agent any
    
    stages {
        stage('testeando el index.html') {
            steps {
                sh '''
                index=/usr/local/apache2/htdocs/index.html
                ws=/var/jenkins_home/workspace/Tarea3
                if [ -e $index ]; then rm -rf $index; fi
                '''
            }
        }
        
        stage('metiendo el index.html en el docker apache') {
            steps {
                script {
                    sh 'cp /var/jenkins_home/workspace/Tarea3/index.html /www/index.html'
                }
            }
        }
    }
}
