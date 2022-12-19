# aws-ansible-provisioning
--
This Ansible playbook prompts the user for their AWS credentials and allows them to select the type of AWS infrastructure they want to build. It then creates the specified infrastructure using the appropriate module. The infrastructure options include an EC2 instance, an RDS instance, or an S3 bucket. The playbook uses variables and 'when' conditions to customize the tasks based on the user's input.
---

This Ansible playbook does the following:

Prompts the user for their AWS access key and secret key. These credentials are needed to authenticate with the AWS API and perform actions on their behalf.

Prompts the user for the type of AWS infrastructure they want to build. The options are 'ec2', 'rds', or 's3'.

Based on the user's selection, it builds the specified AWS infrastructure.

1. If the user selects 'ec2', it creates an EC2 instance using the 'ec2' module.
2. If the user selects 'rds', it creates an RDS instance using the 'rds' module.
3. If the user selects 's3', it creates an S3 bucket using the 's3' module.
4. The playbook uses variables to store the user's input and pass it to the relevant tasks. The 'when' condition is used to specify that a task should only be run if the specified condition is true. In this case, the tasks are only run if the value of the 'infrastructure' variable matches the value specified in the 'when' condition.
