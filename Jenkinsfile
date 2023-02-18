pipeline {
agent any
stages {
    stage('Build') {
        steps {
            sh 'g++ -o PES2UG20CS053-1 hello1.cpp'
        }
    }
    
    stage('Test') {
        steps {
            sh './PES2UG20CS053-1'
        }
    }
    
    stage('Deploy') {
        steps {
            // deployment code
            echo 'Deployment Successful!'
        }
    }
}

post {
    always {
        script {
            if (currentBuild.result == "FAILURE") {
                echo "Pipeline Failed..."
            }
        }
    }
}
}
