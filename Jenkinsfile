pipeline {
    agent any
    tools { 
        maven 'mvn' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn -v'
                sh 'mvn clean install'
            }
        }
    }
}
