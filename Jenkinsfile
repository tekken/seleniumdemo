pipeline {
    agent any
    properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [[$class: 'StringParameterDefinition', name: 'myparam', defaultValue: 'default value']]]])
    stages {
        stage('Build') {
            steps {
                echo "received ${binding.hasVariable('myparam') ? myparam : 'undefined'}"
                echo 'Building my selenium maven tasks'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
