# AWS Instance Connect Demo

### Step 1: Configure network access to your Amazon EC2 instance
* You must configure the following network access to your instance so that you can install EC2 Instance Connect and enable your users to connect to your instance.
* Ensure that the security group associated with your instance allows inbound SSH traffic on port 22 from your IP address.

### Step 2: Install EC2 Instance Connect on an instance
#### For Installation of (Instance Connect) on OS: Amazon Linux 2
```
> sudo yum install ec2-instance-connect
```
