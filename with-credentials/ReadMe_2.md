## This Ansible playbook ```credentialed_awsprov.yml```does the following:

1.  Sets the AWS credentials by reading them from a file at the specified path (`path/to/aws_credentials.yml`).
    
2.  Prompts the user for the type of AWS infrastructure they want to build. The options are 'ec2', 'rds', or 's3'.
    
3.  Based on the user's selection, it builds the specified AWS infrastructure.
    

-   If the user selects 'ec2', it creates an EC2 instance using the 'ec2' module.
-   If the user selects 'rds', it creates an RDS instance using the 'rds' module.
-   If the user selects 's3', it creates an S3 bucket using the 's3' module.

The playbook uses variables to store the user's input and pass it to the relevant tasks. 
The 'when' condition is used to specify that a task should only be run if the specified condition is true. 
In this case, the tasks are only run if the value of the 'infrastructure' variable matches the value specified in the 'when' condition.

### The vars_files directive is used to retrieve the aws_access_key and aws_secret_key variables from the 
```credentialed_awsprov.yml``` file. 

## Make sure to replace path/to/aws_credentials.yml with the actual path to the file.

The aws_credentials.yml file should contain the following variables:

```
aws_access_key: YOUR_ACCESS_KEY
aws_secret_key: YOUR_SECRET_KEY
```

Make sure to replace ```YOUR_ACCESS_KEY``` and ```YOUR_SECRET_KEY``` with your actual AWS access key and secret key.

```credentialed_awsprov.yml``` playbook will first retrieve the AWS credentials from the aws_credentials.yml file,


and then prompt the user for the type of AWS infrastructure they want to build.

Based on the user's input, it will run the appropriate tasks using the ```YOUR_ACCESS_KEY``` and ```YOUR_SECRET_KEY``` to authenticate the AWS modules.
