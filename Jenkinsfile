pipeline {
    agent any
    environment {
        KUBECONFIG = 'C:\\Users\\edwar\\.kube\\config'
    }
    stages {
        stage('Deploy with Helm') {
            steps {
                withCredentials([file(credentialsId: 'kubeconfig-cred-id', variable: 'KUBECONFIG')]) {
                    bat '''
                    set KUBECONFIG=C:\\Users\\edwar\\.kube\\config
                    C:\\ProgramData\\chocolatey\\bin\\helm upgrade --install my-webapp C:\\Users\\edwar\\Documents\\Myworkspace\\Configuration-Management-With-Helm\\helm-webApp\\my-webapp --namespace default
                    '''
                }
            }
        }
    }
}