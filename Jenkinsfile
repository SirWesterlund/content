pipeline {
    agent any
    
    stages {
        stage('comprobando la existencia de index.html') {
            steps {
                sh '''
                index=/var/www/index.html
                ws=/var/jenkins_home/workspace/Tarea3
                if [ -e $index ]; then rm -rf $index; fi
                '''
            }
        }
        
        stage('poniendo el index.html en el docker apache') {
            steps {
                script {
                    sh 'cp /var/jenkins_home/workspace/Tarea3/index.html /www/index.html'
                }
            }
        }
    }
}
