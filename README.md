# AWS
1. Build a Security Group (Port 22 and 80)
2. Build an EC2 Instance (Amazon Linux based 2023)
3. Build a Key Pair
4. Copy and Paste Theo's EC2 Script
5. Launch Instance
6. Copy and Paste Public DNS
7. Paste "http:" - to show EC2 Script WebServer created.
8. SSH into EC2 Instance as it's running
9. Modify EC2 Script and refresh the WebServer page
10. Ping IP address 8.8.8.8 (Google DNS) to show web connectivity.
11. Complete
Security Groups:
1. Build a Security Group (Ports 22 and 80)
* Name: wolfpack-wednesday
* Description: wolfpack-wednesday
* VPC: Leave default
Inbound Rules
* Add Rule
* Type: SSH | Protocol: TCP | Port Range: 22 | Source Type: Anywhere IPv4 | Source: (Default 0.0.0.0) | Description: SSH
* Add Rule
* Type: HTTP | Protocol: TCP | Port Range: 80 | Source Type: Anywhere IPv4 | Source: (Default 0.0.0.0) | Description: HTTP
Outbound Rules
* SKIP OUTBOUND RULES!!!! GO AROUND THEM OR SUFFER THE WRATH OF CHEWBACCA!!!!
Tags
* Key: Name
* Value: wolfpack-wednesday
2. Build an EC2 Instance (Amazon Linux based 2023)
* Click the orange button "Launch instance"
* Name: wolfpack-wednesday
Applications and OS Images (Amazon Machine Image)
* Click the "Quick Start" tab
* Ensure "Amazon Linux" icon is selected
* Amazon Machine Image: "Amazon Linux 2023 kernel-6.1 AMI" (default)
Description: Leave as default
* Instance Type: t3.micro
Key pair (login)
* Click "Create new key pair"
* Key pair name: wolfpack-wednesday
* Key pair type: RSA (leave as default)
* Private key file format: .pem (leave as default)
* Click orange button (Create key pair)
* Save your key pair in your DOWNLOADS folder on your computer
* NOTE: Key pair name is now populated with "wolfpack-Wednesday"
Network Settings:
Network: leave as default
Subnet: leave as default
Auto-assign public IP: should be defaulted as "Enable"
Firewall Security groups:
* Click "Select existing security group"
* Scroll down and click on "wolfpack-wednesday"
Configure storage: leave as default
Advanced details:
* Scroll all the way down to user data (optional)
* (SKIP EVERYTHING BEFORE IT)
* Access the MookieWAF EC2script via GitHub: https://github.com/MookieWAF/bmc4/blob/main/ec2scrpit
* Click the two boxes in the top right corner labeled as "Copy Raw File"
* Look for the pop up box that indicated it was "Copied"
* Go back to your EC2 Instance user data block and paste your script (Ensure the entire script was pasted correctly).
* PRAY TO CHEWBACCA BEFORE YOU LAUNCH INSTANCE!!!
* Click the orange button and Launch Instance at the bottom of the page.
3. Teardown
* Go to your EC2 Instance. Go to Action and click "Terminate Instance.
* Go to your Security Group, click the Action button at the top and click "Delete Security Group"
* Praise Chewbacca and Get this Money
