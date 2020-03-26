node { 
    stage(' Example' ) {
        git branch: 'develop', credentialsId: 'GitHubCredentials', url: 'https://github.com/aaron070596/CodeWarsIssues.git'
        sh label: 'Showing Data', script: 'ls -la'
    }
}