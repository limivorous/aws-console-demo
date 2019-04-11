# AWS Console Demo
## Preamble
This is a series of demos designed to show some of the capabilities of AWS, using the console as much as possible, to an audience new to AWS.  
Although the majority of the steps are done through the console certain shortcuts have been taken to make the demo easier to consume.


## Requirements
You should already have an account created. Ideally this will a new, or empty, account to save on any confusion within the demo that could be created by existing resources.  
The demo will create assets within your account some of which will be chargeable; it is up to the user of these instructions/scripts to remove assets once they are finished with them. Notes will be made to remind the user to remove the assets at the end of the demo.

There should already be some form or remote desktop client installed on your machine. If you are using a windows based machine then this will already be present. If you are using a mac then please install; 
Microsoft Remote Desktop for Mac.
https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/remote-desktop-mac

Depending on your choice you should also have a Yubikey (hardware) or Google Authenticator installed on your phone (Software). This will be used for 2 Factor Authentication during one of the demos.


## Setup
Prior to running any of the demos you should run some initial setup steps. These steps create networking and security components that are required but technical in nature.

### All demos setup
Login to the account you are going to use for the demonstration as the root/admin of the account.  
You can either use Launch button below (only Ireland is currently supported) or run the template manually in your account.  

Stack| Launch
------|-----
EU (Ireland) | [![Launch Demo in eu-west-1](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformation-launch-stack-button.png)](https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/new?stackName=ConsoleDemo&templateURL=https://s3-eu-west-1.amazonaws.com/github-limivorous/aws-console-demo/1.setup_cf.yaml)


If you wish to run is manually the cloudformation template 1.setup_cf.yaml is contained here:  
[http://www.github.com/limivorous/aws-console-demo/Cloudformation/1.setup_cf.yaml](http://www.github.com/limivorous/aws-console-demo/Cloudformation/1.setup_cf.yaml)

## Available demos
Once the above steps have been completed there are 4 demos which can be run starting with the introduction demo.  
You must run the introduction demo first and then run whichever of the others you wish. You MUST run the demos in the same region where the cloudformation template (above) was run.
1. [IAM & EC2 Demo](Documentation/1.IAMEC2.Demo.md)
2. [RDS] - In Progress
3. [CloudTrail] - In Progress
4. [S3 Demo](Documentation/4.S3.Demo.md)
