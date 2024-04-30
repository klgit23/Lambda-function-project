# Lambda Function
## Setup
- [x] Install boto3: (using python v3.8.1) boto3 is aws sdk for python. Pip install boto3; then pip show boto3 to view boto3 info
<img src="https://github.com/klgit23/proj1-docker-projects/assets/154713258/7a258952-9973-49a5-9621-05cb925611a9" width="50%">

- [x] IAM user: a user with AdministorAccess
- [x] Configure aws cli: use aws configure to set up profile; use aws sts get-caller-identity to confrim the identity being used
- [x] Install vs code extensions: Jupyter, Pylance
- [x] Install Git and sign up with Github account
- [x] Create SSH key pair (in window powershell) ssh-keygen -t rsa -b 2048; -> add SSH public key to Github 
- [x] Create and clone a Git repository: create a repository in github, then use git clone to clone this repo to local (use the SSH link not HTTPS link from github site, as we have set up SSH in previous steps)
- [x] Python script: in vs code
## Project 1 Objective (from AOS Note project): 
### when a files move to S3 buckent, a lambda function is triggered to move the file to a folder with folder name as YYYYMMDD/filename. YYYYMMDD is the time when the file is created.
### Steps
* Get today’s date and format as 	"%Y%m%d"
* In lambda_handler function
  - List all folder names insdie the bucket: if no such folder as “YYYYMMDD/” exists, then create such a folder; if such a folder already exists, then list all objects inside this folder,
  - Write a for loop to go over each file’s name, if the file’s last modified date is today and its name doesn’t contain “/”, then copy the file to the folder with name “YYYYMMDD/” and delete original file.
 
## Project 2 Objective (based on Rajdeep Saha project): 
### AWS API gateway – Lambda function – DynamoDB microservices; lambda function to get and post item in DynamoDB table.
### Steps
<img src="https://github.com/klgit23/proj1-docker-projects/assets/154713258/9692644e-ee0f-4b8c-9f63-e91e928e8d09" width="30%" height="40%">

<img src="https://github.com/klgit23/proj1-docker-projects/assets/154713258/00ed1a04-3054-4346-87b6-0c37bcc50477" width="30%" height="40%">

* Lambda_handler function
 
  <img src="https://github.com/klgit23/proj1-docker-projects/assets/154713258/35997998-ce8c-4303-9152-724b72d9cafe" width="60%" height="60%">


  
