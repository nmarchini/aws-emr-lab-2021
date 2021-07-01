
# aws-emr-lab-2021
Supplemental instructions for EMR lab

The lab [here](https://emr-etl.workshop.aws/) from AWS for setting up an EMR Cluster assume that you have already complete some steps, I have no idea where these steps are but here are the missing bits of information you need to be able to complete this lab successfully. 

### Cloud9 setup

 - Make sure you are in the N.Virginia region if using EventEngine as the AWS account provider
 - In the AWS Console navigate to Cloud9 ( search for Cloud9 in the main
   search box at the top of the AWS console) and click on **Create
   Environment**
   
 - Enter a Name for the environment (emr-lab), Click **Next Step**
 - Set the following values for each section
	 - Environment Type = Create a new no-ingress EC2 instance for environment (access via Systems Manager)
	 - Instance type = t2.micro
	 - Platform = Amazon Linux 2 (recommended)
 - Leave other settings as default and click **Next Step**
 - On the review screen review the information is correct and then click **Create Environment**
 - After a few minutes you will see the Cloud9 welcome screen. Keep this browser window open and continue to the next step	 
	  

### SSH Key
For this lab we are using  the EventEngine facility provided by AWS, the instructions below show you how to get the SSH key where you need it to be able to run the lab. The lab advises you to use Cloud9. 

 - From the EventEngine Team Dashboard click on the **SSH Key** button
 - Click the Download Key button to download the key file to your local machine
 - Click back to your Cloud9 browser window and click on the **File** menu button, then select **Upload Local files**
 - Either drag the ssk key file to the Upload file window or use the **Select files** button to locate it. 
 - Once the file is uploaded you will see it in the folder navigation window on the left side of the screen
 - Find the Terminal window in the Cloud9 browser, it is at the bottom of the screen, you can drag the window divider to maker it larger to view. You should see a prompt like `TeamRole:~/environment $`
 - Enter the following command and press enter `chmod 400 <name of key pair>`
	 - `chmod 400 ee-default-keypair.pem`


