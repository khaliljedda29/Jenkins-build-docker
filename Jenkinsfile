node {
    def app

    stage('Clone') {
        checkout scm
}
    stage('Build image') {
        app = docker.build(khalil/nginx)
}
    stage('Run image') {
         docker.image('khalil/nginx').withRUN('-p 80:80') { c ->
	sh 'docker ps'
	sh 'curl localhost'
}
}
