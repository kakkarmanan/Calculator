pipeline {
    agent {
        label 'master'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
        // stage('Sonar-Report') {
        //     steps {
        //     sh 'mvn clean install sonar:sonar -Dsonar.host.url=http://localhost:9000/ -Dsonar.analysis.mode=publish'
        //     }
        // }
        stage('Test') { 
            steps {
                bat 'mvn test' 
            }
            // post {
            //     always {
            //         junit 'target/surefire-reports/*.xml' 
            //     }
            // }
        }
        // stage('Deploy'){
        //     steps{
        //         sh '/var/deployment/./deployment.sh'
        //     }
        // }
    }
}
