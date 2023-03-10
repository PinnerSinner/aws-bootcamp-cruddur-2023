# Week 0 — Billing and Architecture

## Summary 

Following our livestream induction, I'm thrilled to begin the design phase of the Cruddr app and commit to the build process!
I found the session to be engaging and explained well the bootcamp's structure going ahead. It'll be on Saturdays (early evening for myself in the UK timezone) for the next 14 weeks with follow-up videos to follow-up on with concepts that weren't covered in-class, as well as homework to document the build process going ahead. 

## The bootcamp's business concept
- "You have been hired as a new Employee on a startup. As a cloud engineer interviewed by a co-founder, you will handle the app project using a microservice that can leverage the decoupling of components so that the app will survive in case of a disaster strike. You ask what are microservices and their benefit from your projects and the Co-Founder tells you about Agility, Easy Deployment, Technological Freedom from other providers, and also flexible scaling."
- The “Iron Triangle” maps quality with proportion to Cost, Time, and Scope. 


## What I've learnt:
- Firstly, I've brushed up on writing in MarkDown. It's not something which I've used in practice before, but seems to be the convention for writing documentation in Github repos.
-- My syntax and code will be something which will improve over time, although it doesn't seem to be a steep learning curve. This being my first time actually using Git, but won't be the last!
-- For example, `This is an example of a code block using Typescript`
-- I'm considering using the `![alt text](www._____.com)`tool in order to host and display images & screenshots from my ongoing homework. 
- I learned how to clone a template and create a new Git repository. Case in point, here. Ta-da!

# Homework Hard Assignments
1) SET BUDGET & BILLING ALARM - I set up a budget to better track my monthly spend. The budget threshold is at 80% which pushes an SNS email notification when this threshold is breached. 
- Since I'm paying for a Skillsbuilder subscription (which tends to sum at $36 dollars monthly) as well as a few customer-managed KMS keys which I'm using in my own account, then I'm setting my budget to $40 since I am expecting some costs.
- I do have a few months left of my Free Tier account, but for simplicity I'm going to keep using this account for now instead of opening up a new account. 
- I've set a separate budget for credits which is capped at $1.00. 
-- [![Opera-Snapshot-2023-02-12-174227-us-east-1-console-aws-amazon-com.png](https://i.postimg.cc/kgXD05tT/Opera-Snapshot-2023-02-12-174227-us-east-1-console-aws-amazon-com.png)](https://postimg.cc/WhC2rT8Z)

2) GENERATING AWS CREDENTIALS
- I installed the AWS CLI to my local desktop's GitPod. 
- When testing out Powershell, I found the --cli-auto-prompt rather helpful. Its command-completion feature either automatically completes my command or displays a suggested list of commands. 

-- [![Opera-Snapshot-2023-02-12-174947-us-east-1-console-aws-amazon-com.png](https://i.postimg.cc/g0sCfY8H/Opera-Snapshot-2023-02-12-174947-us-east-1-console-aws-amazon-com.png)](https://postimg.cc/QBBY7Z6F) 
- I used this to generate my account caller identity, as well as to get my account contact information. 
- Powershell is useful from within the account, but I wanted to have an SSH connection directly pointing to my local machine. 
- In my GitPod terminal, I fed `curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install` 
- [![image-2023-02-12-175818259.png](https://i.postimg.cc/t70PpGWB/image-2023-02-12-175818259.png)](https://postimg.cc/xNRq37sm)
- I didn't want to commit this to my repo, but rather just install the CLI. So I went back into my workspace and curl downloaded the CLI. 
- Ran the bash script which installed the AWS CLI on GitPod
- [![image-2023-02-12-183819696.png](https://i.postimg.cc/gjct85Jc/image-2023-02-12-183819696.png)](https://postimg.cc/S25GpgCH)

3) Create an architectural diagram in Lucid Charts:
-- Conceptual diagram 
[![image-2023-02-17-184135578.png](https://i.postimg.cc/rF718nsF/image-2023-02-17-184135578.png)](https://postimg.cc/VdBrgFX3)
https://lucid.app/lucidchart/a3fef105-c8d9-4f5d-bf0d-fec70103c96b/edit?viewport_loc=-549%2C-117%2C3017%2C1068%2C0_0&invitationId=inv_ac74098b-e5b9-426b-8a47-574d05774e73
-- Logical diagram
[![image-2023-02-17-193846097.png](https://i.postimg.cc/25WzgfSm/image-2023-02-17-193846097.png)](https://postimg.cc/068RJFSH)
[https://lucid.app/lucidchart/54816248-6870-479b-848d-5f9420add748/edit?viewport_loc=-11%2C-64%2C2164%2C1068%2C0_0&invitationId=inv_694ea032-edf0-454b-b46e-dbdaf52922ab
](https://lucid.app/lucidchart/54816248-6870-479b-848d-5f9420add748/edit?viewport_loc=217%2C-8%2C2164%2C1068%2C0_0&invitationId=inv_694ea032-edf0-454b-b46e-dbdaf52922ab)



# Homework Stretch Assignments
1) DESTROY ROOT ACCOUNT CREDENTIALS, SET MFA, IAM ROLE
- I've locked down my admin account with an MFA device, as well as cleaned up any unused access keys for the CLI. 
-- [![Opera-Snapshot-2023-02-12-172550-us-east-1-console-aws-amazon-com.png](https://i.postimg.cc/Hx0pJ4CT/Opera-Snapshot-2023-02-12-172550-us-east-1-console-aws-amazon-com.png)](https://postimg.cc/BL6WkF6z) 
-  

 2) 4Cs considerations 
[![IMG20230217194828.jpg](https://i.postimg.cc/nrmVfbkq/IMG20230217194828.jpg)](https://postimg.cc/BPqf2zRv)
