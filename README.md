## **Apache webserver, using Terraform and configured with Ansible Playbook**
A project where I aimed to deploy example networking resources and an EC2 instance using Terraform and configure it as an Apache webserver, using an Ansible playbook to install the required service and sideload the website build from S3

### **Description:**
1. Create VPC, Internet Gateway, Route table, Subnet, Security Group for the VPC, Network interface and Elastic IP
2. Associate the Route Table with the subnet and the elastic IP with the Network Interface
3. Create the EC2 instance
4. Use the remote-exec provisioner to run a shell script which enables Terraform to wait for Cloud-init
5. Use the local-exec provisioner to run the Ansible playbook, which installs the httpd service, sideloads the build from an S3 bucket and makes sure the service is running
