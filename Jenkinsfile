pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git credentialsId: 'd9c3df91-0beb-4636-ae2a-8d1724af1e38', url: 'https://github.com/ratatouka/devops.git'
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    echo 'done'
                }
            }
        }
    }
}
