# Interview
DevOps skills Interview

# Instructions:
This is a practical exercise to test your DevOps and AWS knowledge. You may use the internet and AWS documentation to complete this task. You are required to complete the following steps:

Use as much time as you need to research & ask us questions as you go through the process.

EXERCISE 1) Create a custom VPC in us-west-2 region with a public and a private subnet using AWS Web interface 
(AWS Web Admin Console). 

    GOAL: Launch an EC2 and install nginx to display a functional webserver accessible by browser
        a) the EC2 must be created in a private VPC
        b) USE the CIDR 10.55.0.0/16 to build your vpc, build the vpc in us-west-2
        c) A Loadbalancer must be used to front the traffic
        d) Add as much security into your design as possible
        e) SSL Certificates of any kind & PORT 443 configuration not necessary due to time constrai
        Goal considered finished when the website is accessible via web browser

EXERCISE 2) IaC - We have a CloudFormation template in both JSON or YAML formats (your preference) 
which satisfies the following requirements:

    a) Use the VPC Resources from EXERCISE [1] to launch two AWS Linux EC2 instances:
    You must configure your shell environment to run commands to run cloudformation
    You have permission to create access keys
      * One instance is publicly available which should act as a bastion.
      * The second instance is a private instance and should act as an apache http web server.
    
    NOTES: 
    - You will need to automate the configuration of both instances 
    using userdata in the cloudformation template. 
    The template is broken and has missing details.
    - If you are on a windows machine, you can attach an IAM role called 'encrypt-at-rest' 
    to an ec2 machine and perform shell environment configurations on that ec2 machine

    b) Create a load balancer that can serve the web page coming from the 
    apache web server in the private subnet.
    c) Proof that it works by showing us the web page in a browser. 
    d) SSH into the bastion to do the following:
    - install and configure ansible to be able to access the private instance
    - Clone this repo, review and run the playbook in this repository 
    to modify the web page 
    served by the private instance.
    e) SSH to the private instance to do the following tasks:
    - Check if the web page change has been applied
    - Check the web page from the browser.

EXERCISE 3) Ansible
    a) SSH into the public instance and do the following:
        We would like you to install ansible(any version), 
        and then configure ansible to run and install a package 
        called 'htop' on the current ec2 machine
    BONUS EXERCISES:
    b) Install the specific version of ansible, ansible version 2.7.5
    c) Access the Ansible playbook, understand what it does and change 
    what is necessary in Ansible configuration. Run the playbook.
