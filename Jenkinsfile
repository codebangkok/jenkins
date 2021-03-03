import groovy.json.JsonSlurper

node("go_labels") {
    stage("Clone") {
        git branch: 'bannasarn', url: 'https://github.com/codebangkok/jenkins'
    }
    stage("Build") {
        sh "go build src/goapp/main.go"
    }
    stage("Test") {
        sh "go test src/goapp/main.go"
    }
}