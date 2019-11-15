# Security Compliance CloudFormation Template
## A SSM-powered Security Compliance CloudFormation Template

For creating an SSM association task to scan Windows and Linux VMs matching specific tags for Security Compliance based on Dev-Sec baseline and patch-baseline.
The SSM association task runs on a scheduled basis which is defined by the `CronExpression`.

## Input Parameters:
- `LinuxTagKey` - List of tags used by Linux EC2 instances, defaults to `linux,lin`
- `WindowsTagKey`   - List of tags used by Windows EC2 instances, defaults to `windows,win`
- `InstanceTagKey`          - Tag key used to specify EC2 instances, defaults to `os`
- `CronExpression`  - Cron expression for SSM association scheduled run. Default is `"0 16 ? * TUE *"`

## Example usage
```
aws cloudformation deploy --stack-name="security-compliance" --template-file=security_compliance.yaml 
```


## Links

https://dev-sec.io/

https://docs.aws.amazon.com/systems-manager/latest/userguide/integration-chef-inspec.html
