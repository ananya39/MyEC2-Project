Steps to Host a Website on AWS EC2   
Step 1: Launch an EC2 Instance
 
<< Log in to your AWS Management Console.

<< Go to EC2 Dashboard → Launch Instances.

<< Choose Amazon Linux as the AMI (Amazon Machine Image).

<< Select the instance type (e.g., t2.micro for free tier).

<< Configure security group to allow HTTP (port 80) and SSH (port 22).

<< Launch the instance and download the private key (.pem file).

Step 2: Connect to Your EC2 Instance
 
 << Open Git Bash or any terminal.
 
 << Connect using SSH
 
    ssh -i privateKey.pem ec2-user@YourPublicIP
    
Step 3: Install Apache HTTP Server
 
 << Update the instance:
 
  sudo yum update -y
  
 << Install Apache:
 
  sudo yum install -y httpd
  
<< Start Apache and enable it to run on boot:

   sudo systemctl start httpd
   
   sudo systemctl enable httpd
   
Step 4: Create a Simple Website
 
<< Navigate to the web server directory:

   cd /var/www/html
   
<< Create an index.html file:

   sudo nano index.html
   
<< Add simple HTML content

<< Save and exit using Ctrl + O → Enter → Ctrl + X.
