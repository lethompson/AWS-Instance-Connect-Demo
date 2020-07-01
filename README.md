# AWS Instance Connect Demo
## Prequisites for using Amazon Instance Connect
* Create an IAM user that has AWS CLI or Console Access or both
* Create an inline policy to configure IAM permissions for EC2 Instance Connect for your IAM user

### Inline policy for IAM user
```
{
    "Version": "2012-10-17",
    "Statement": [
      {
        "Effect": "Allow",
        "Action": "ec2-instance-connect:SendSSHPublicKey",
        "Resource": [
            "arn:aws:ec2:region:account-id:instance/i-1234567890abcdef0",
            "arn:aws:ec2:region:account-id:instance/i-0598c7d356eba48d7"
        ],
        "Condition": {
            "StringEquals": {
                "ec2:osuser": "ec2-user"
            }
        }
      },
      {
        "Effect": "Allow",
        "Action": "ec2:DescribeInstances",
        "Resource": "*"
      }
    ]
}
```

### Step 1: Configure network access to your Amazon EC2 instance
* You must configure the following network access to your instance so that you can install EC2 Instance Connect and enable your users to connect to your instance.
* Ensure that the security group associated with your instance allows inbound SSH traffic on port 22 from your IP address.

### Step 2: Install EC2 Instance Connect on an instance
#### For Installation of (Instance Connect) on OS: Amazon Linux 2
```
> sudo yum install ec2-instance-connect
```
