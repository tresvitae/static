pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(region:'us-west-2', credentials:'aws-static') {
                sh 'echo "Uploading index.html to S3 Bucket"'
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udacity-project-jenkins-pipelines-tresvitae')
			}
		}
	}
}