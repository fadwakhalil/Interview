# Interview
DevOps skills Interview

# Instructions:
This is a 1 hour practical exercise to test your AWS knowledge. You may use the internet and AWS documentation to complete this task. You are required to complete the following steps:

1. Create a custom VPC in us-west-2 region using the aws console, with a public and a private subnet. 

2. We have a CloudFormation template in both JSON or YAML formats (your preference) which satisfies the following requirements:

    - Starts two AWS Linux EC2 instances:
      * One instance is publicly available which should act as a bastion.
      * The second instance is a private instance and should act as an apache http web server.
    
    You will need to automate the configuration of both instances using userdata in the cloudformation template
    You will need to go through . the template is broken and has several missing details.

3. Create a load balancer that can serve the web page coming from the apache web server in the private subnet.
4. Proof that it works by showing us the web page in a browser. 
