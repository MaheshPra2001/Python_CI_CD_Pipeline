pipeline {
        agent any // Specifies where the pipeline will run (any available Jenkins agent)

        stages {
            stage('Build') { // Defines a stage named 'Build'
                steps {
                    sh 'mvn clean install' // Executes shell commands within the stage
                }
            }
            stage('Test') {
                steps {
                    sh 'mvn test'
                }
            }
            stage('Deploy') {
                steps {
                    echo 'Deploying application...'
                }
            }
        }

        post { // Defines actions to be executed after all stages
            always {
                echo 'Pipeline finished.'
            }
            success {
                echo 'Pipeline succeeded!'
            }
            failure {
                echo 'Pipeline failed!'
            }
        }
    }