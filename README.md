## aws
aws ansible scripts
==============

This repository includes some sample codes to show how to create AWS resources, such as VPC, subnet, route table, security group, EC2, ELB, with ansible playbooks and roles.
.
├── credentials.yml
├── inventory
├── playbook.yml
├── README.md
└── roles
    ├── ec2
    │   ├── tasks
    │   │   └── main.yml
    │   └── vars
    │       └── main.yml
    ├── ELB
    │   ├── tasks
    │   │   └── main.yml
    │   └── vars
    │       └── main.yml
    └── vpc
        ├── tasks
        │   └── main.yml
        └── vars
            └── main.yml

Free feel to use these scripts to learn ansible and aws. Star and fork if you think it is helpful. Thanks.

In order to run these ansible playbooks and roles, you need to have boto/boto3 and aws cli pre-installed. 
# Prerequisites
Boto: 
```
sudo pip install boto
```
AWS cli:
```
sudo pip install awscli
```

# How to use
Use Git to clone the repository:
```
git clone https://github.com/devopscripts/aws.git
```
```
Put your keys into credentials.yml as variables.
---
#aws credentials
aws_access_key: "your_access_key"
aws_secret_key: "your_secret_key"
key_name: "your_key_pair(ssh_key)"
```
Run the below command to set up VPC, ec2, ELB, subnet, security group ...
```
ansible-playbook playbook.yml -i inventory -e @credentials.yml
```

# Submit bugs:
Please use https://github.com/devopscripts/aws/issues to submit your comments and bugs found. Thanks for your feedback.
