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
	stage('Backup') {
		steps {
			sh 'scp -P 1980 output.txt jakieabedin@0.0.0.0:135:/C:/Users/jabedin/'
		}
	}
    }
}
