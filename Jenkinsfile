pipeline {

agent any


stages {


stage('Clone Code') {

steps {

echo "Pulling code from Github"

}

}


stage('Deploy To Nginx') {

steps {

sh '''

scp -r * ubuntu@32.196.165.132:/var/www/html/

'''

}

}


}


}
