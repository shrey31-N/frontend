pipeline {

agent any


stages {


stage('Checkout Code') {

steps {

echo "Code downloaded from Github"

}

}



stage('Deploy To S3') {


steps {

sh '''

aws s3 sync . s3://uniqfrontend --delete

'''

}

}



stage('CloudFront Cache Clear') {


steps {


sh '''

aws cloudfront create-invalidation \
--distribution-id E3H3XP5JGGW4N7 \
--paths "/*"

'''

}


}


}


}
