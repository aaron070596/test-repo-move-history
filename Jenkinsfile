node { 
    stage(' Example' ) {
        git branch: 'develop', credentialsId: 'GitHubCredentials', url: 'https://github.com/aaron070596/CodeWarsIssues.git'
        sh label: 'Showing Data', script: 'ls -la'
    }

    stage(' api Call' ) {
        def apiResponse =  httpRequest 'https://jsonplaceholder.typicode.com/todos/1'
        echo "this is the  final  result ${apiResponse.content}"
    }

    stage(' clean workspace' ) {
        cleanWs() 
    }

    stage(' clean workspace' ) {
        emailext body: 'pass', subject: 'succes job', to: 'aaron070596@gmail.com'
    }

}