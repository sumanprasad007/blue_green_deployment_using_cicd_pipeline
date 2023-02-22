Blue-Green Deployment
This repository contains a script for a Blue-Green Deployment, which is a technique for releasing software with minimal downtime.

Installation
The user-data script in this repository installs Apache and creates an index.html file in the /var/www/html directory. It also installs the CodeDeploy agent and sets up auto-update. The script is designed to run on Ubuntu or Amazon Linux.

To use this script, copy the contents of the user-data file and paste them into the user-data field when launching an EC2 instance.

Usage
To use the Blue-Green Deployment technique, you need two sets of identical infrastructure, one of which is currently live (the blue environment), and the other which will become the new environment (the green environment).

The steps for the deployment are as follows:

Start up the green environment and run any tests to ensure it is working correctly.
Switch the load balancer to route traffic to the green environment.
Stop the blue environment.
If there are any issues with the green environment, the load balancer can be switched back to the blue environment to revert the deployment.

License
This project is licensed under the MIT License.# blue_green_deployment_using_cicd_pipeline
