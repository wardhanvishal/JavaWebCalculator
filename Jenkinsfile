pipeline {
    agent any

    stages {
        stage('CompileJob') {
            steps {
		echo 'code validate'
		sh 'mvn validate'
            }
        }
        stage('UnitTest') {
            steps {
		echo 'code test'
		sh 'mvn test'
            }
        }
        stage('SonarAnalysis') {
            steps {
		 echo 'code analysis'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://3.83.157.27:9000 -Dsonar.login=c49bb93bf286b60a5ff58cb47cb68394a06b3284'
            }
        }
    }
}
