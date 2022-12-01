# aws_codedeploy_using_github
Create two IAM role 1st for Codedeploytoec2 and 2nd for CodeDeploy
Create the Ec2 instance and attach role [Administrator access like. Codedeploy to ec2]
run following command in created instance - 
sudo yum update
sudo yum install ruby
sudo yum install wget
crate .sh file and add following content
[#!/bin/bash
CODEDEPLOY_BIN="/opt/codedeploy-agent/bin/codedeploy-agent"
$CODEDEPLOY_BIN stop
yum erase codedeploy-agent -y]
and run now
wget https://aws-codedeploy-us-east-1.s3.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
sudo service codedeploy-agent status
sudo yum install -y python-pip
sudo pip install awscli
then create codedeploy and create codepipeline
Use this url for any error [https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-verify.html]
