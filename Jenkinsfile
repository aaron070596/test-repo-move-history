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
        mail bcc: '', body: 'hi', cc: '', from: '', replyTo: '', subject: 'todos', to: 'aaron070596@hotmail.com'
    }

}