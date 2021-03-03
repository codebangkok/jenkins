import groovy.json.JsonSlurper

node("docker_labels") {
    stage("Clone") {
        git branch: 'bannasarn', url: 'https://github.com/codebangkok/jenkins'
    }
    stage("Build") {
        sh "docker image build -t codebangkok/goapp src/goapp"
    }
    stage("Push") {
        sh """
            docker login -u codebangkok -p Infinitas2021
            docker image push codebangkok/goapp
        """
    }
}