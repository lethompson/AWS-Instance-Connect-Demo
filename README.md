# AWS Instance Connect Demo
## Prequisites for using Amazon Instance Connect
* Create an IAM user that has AWS CLI or Console Access or both
* Configure IAM permissions for EC2 Instance Access for your IAM user

### Step 1: Configure network access to your Amazon EC2 instance
* You must configure the following network access to your instance so that you can install EC2 Instance Connect and enable your users to connect to your instance.
* Ensure that the security group associated with your instance allows inbound SSH traffic on port 22 from your IP address.

### Step 2: Install EC2 Instance Connect on an instance
#### For Installation of (Instance Connect) on OS: Amazon Linux 2
```
> sudo yum install ec2-instance-connect
```
### Step 3: Connect using the browser-based To connect to your instance using the browser-based client from the Amazon EC2 console

* Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/
* In the navigation pane, choose Instances.
You can connect to an instance using the browser-based client by selecting the instance from the Amazon EC2 console and choosing to connect using EC2 Instance Connect. Instance Connect handles the permissions and provides a successful connection.

#### To connect to your instance using the browser-based client from the Amazon EC2 console

* Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/
* In the navigation pane, choose ```Instances```.
* Select the instance and choose ```Connect```.
* Choose EC2 Instance Connect ```(browser-based SSH connection), Connect```.
