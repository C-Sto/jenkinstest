properties([parameters(
[
    string(defaultValue: '127.0.0.1', description: 'Build Server', name: 'toolsServer')
]
)])


if (params.toolsServer.trim() == "" ) {
    throw new Exception("Build Server Name required")
}

node {
   stage('Preparation') {
      echo "Checking out: ${params.toolsServer}"
   }

   stage('Build Container Image') {
        println "Build container Image ${params.toolsServer}"
        sh "echo 'test ${params.toolsServer}:5000/ok'"
   }
}