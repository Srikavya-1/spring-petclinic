pipeline { agent any

stages {
    stage('Clone') {
        steps {
            git branch: 'feature/2025.03.14', url: 'git@github.com:Srikavya-1/spring-petclinic.git'
        }
    }
    stage('Build') {
        steps {
            sh 'mvn package'
        }
    }
    
    stage('Test') {
        steps {
            sh 'mvn test'
        }
    }
    stage('Test Results Reports') {
        steps {
            junit 'target/surefire-reports/*.xml'
        }
    }
    
    stage('Artifacts') {
        steps {
            archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
        }
    }
    stage('Deploy') {
        steps {
            echo 'Hello World'
        }
    }
}
}