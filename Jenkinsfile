properties([pipelineTriggers([githubPush()])])

node('linux') {
    git url: 'https://github.com/AnakinTang/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
}