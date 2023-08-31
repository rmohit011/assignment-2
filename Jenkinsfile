pipeline {
    agent any
    
    parameters {
        string(name: 'PARAMETER_NAME', defaultValue: 'default_value', description: 'Description of the parameter')
        choice(name: 'CHOICE_PARAMETER', choices: ['Option 1', 'Option 2', 'Option 3'], description: 'Select an option')
        booleanParam(name: 'BOOLEAN_PARAMETER', defaultValue: true, description: 'Enable or disable something')
    }
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Accessing the parameters within the Groovy script
                    def paramValue = params.PARAMETER_NAME
                    def choiceValue = params.CHOICE_PARAMETER
                    def booleanValue = params.BOOLEAN_PARAMETER
                    
                    echo "Parameter Value: ${paramValue}"
                    echo "Choice Parameter Value: ${choiceValue}"
                    echo "Boolean Parameter Value: ${booleanValue}"
                    
                    // Your build steps here
                }
            }
        }
        
        // Add more stages as needed
    }
    
    post {
        always {
            // Cleanup or final steps to execute regardless of build success or failure
        }
    }
}
