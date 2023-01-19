## Minimum security baseline. How to improve your security posture with a minimum security baseline artifact

This is a set of cloudformation templates that enables a minimum security baseline in a new AWS account that doesn't have Amazon GuardDuty, AWS Security Hub, Amazon Macie, Password Policy and Access Analyzer enabled.

The solution is considered to be part of an integral security program.
Instructions:
- Create S3 bucket in your AWS account
- Upload templates:
   - plantilla-raiz.yml
   - plantilla-parametros.yml
   - plantilla-llaves.yml
   - plantilla-buckets.yml
   - plantilla-seguridad.yml
   - plantilla-notificaciones.ymkl
   - plantilla-cis-alerts.yml
   - plantilla-cis-dashboard.yml
   - iam-security-policy.yml
   
In AWS Cloudformation launch template root-stack.yml and provide parameters:
  - AbreviaturaCuenta. Name for your AWS account. Input any lower case characters. 
  - BucketPlantillas. S3 bucket where templates were stored.
  - CorreoCotificacion. Email to send events notifications.
  - CISDashboard. Select true if you want to enable CIS control dashboard.
  - GuardDuty. Select true if you want to enable Amazon GuardDuty.
  - Macie. Select true if you want to enable Amazon Macie.
  - SecurityHub. Select true if you want to enable AWS Security Hub. 
  
  All other parameters are optional
  Advance additional steps and acknowledge creation of IAM resources and Capability_auto_expand in final step.

If you have Amazon GuardDuty, AWS Security Hub, Amazon Macie, Password Policy and Access Analyzer enabled, you should modify seguridad.yml to not enable a specific service or it will break.

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

## Content Security Legal Disclaimer

“The sample code; software libraries; command line tools; proofs of concept; templates; or other related technology (including any of the foregoing that are provided by our personnel) is provided to you as AWS Content under the AWS Customer Agreement, or the relevant written agreement between you and AWS (whichever applies). You should not use this AWS Content in your production accounts, or on production or other critical data. You are responsible for testing, securing, and optimizing the AWS Content, such as sample code, as appropriate for production grade use based on your specific quality control practices and standards. Deploying AWS Content may incur AWS charges for creating or using AWS chargeable resources, such as running Amazon EC2 instances or using Amazon S3 storage.”
