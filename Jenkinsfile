properties([pipelineTriggers([githubPush()])])

node('linux') {
    git url: 'https://github.com/AnakinTang/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
    
    stage('GetInstances') {
        sh "aws ec2 describe-instances --region us-east-1"
        sh "hello world"
    }
    
    stage('CreateInstance') {
        sh "aws ec2 run-instances --image-id ami-467ca739 --count 1 --instance-type t2.micro --key-name classroom --security-group-ids sg-5cde582b --subnet-id subnet-d573ae9f --region us-east-1"
    }
}
