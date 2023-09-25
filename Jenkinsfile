pipeline{
    agent any
    stages{
        stage('code checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/anoopkmathew4u/django-web-app.git'
            }
        }
        stage('build'){
            steps{
                script{
                    sh "docker build -t anoop/djangoapp ."
                }
            }
        }
        stage('deploy'){
            steps{
                script{
                    sh "docker run -p 8000:8000 -d anoop/djangoapp"
                }
            }
        }
    }
}
