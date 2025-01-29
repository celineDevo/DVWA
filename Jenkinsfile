pipeline {
    agent any

    stages {
        stage('Checkmarx AST analysis') {
            steps {
                checkmarxASTScanner additionalOptions: "--threshold \"sast-high=10; sast-medium=20; sca-high=10\"  --report-format sarif  --output-name \"dvwa_results\"", 
                baseAuthUrl: '', 
                branchName: 'master', 
                checkmarxInstallation: 'CxOne', 
                credentialsId: '', 
                projectName: 'DVWA', 
                serverUrl: '', 
                tenantName: '', 
                useOwnAdditionalOptions: true
            }
        }
    }
}