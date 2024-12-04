pipeline {
    agent any
    environment {
        REPO = "devopsity22/caesar-cipher"
    }

    stages {
        stage('build') {
            steps {
                sh 'chmod +x gradlew'
                sh './gradlew clean build'
            }
        }
        stage('test') {
            steps {
                sh './gradlew test'
                sh 'java -jar build/libs/caesar-cipher.jar'
            }
        }
        stage('Release') {
            steps {
		sh 'printenv'
                            
	}
        }
	stage('Health Check') {
		steps {
			sh 'curl -f http://localhost:8080/health || exit 1'
		}
	}
    }
}
