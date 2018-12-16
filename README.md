# AWS Transfer for sFTP requirements

The CloudFormation template contains all requirements to configure AWS Transfer for sFTP if you use "Service managed" as the identity provider.

* AWS S3 bucket
* IAM role for sFTP server logging to AWS CloudWatch
* IAM role for access role for the user

The "Service managed" identity provider works with SSH keys. To generate the ssh keys just use the following command:

```ssh-keygen -P "" -f transfer-key```

Copy the content of the generated file "transfer-key.pub" into the AWS console field "SSH public key".
