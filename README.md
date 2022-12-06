## Minimum security baseline

This is a set of cloudformation templates that enables a minimum security baseline in a new AWS account that has no services enabled.
The solution is considered to be part of an integral security program.
Instructions:
- Create S3 bucket uin your AWS account
- upload the templates
   - root-stack.yml
   - plantilla-parametros.yml
   - plantilla-llaves.yml
   - plantilla-buckets.yml
   - plantilla-seguridad.yml
   - plantilla-notificaciones.ymkl
In AWS Cloudformation launch template root-stack.yml and provide parameters:
  - bucket-plantillas - ths is the name of the s3 bucket where the cloudformation templates are stored
  - abreviaturacuenta - this is an abreviation for your AWS account identification, it is used as part of the name on some of the created resources
  - correonotificacion - email to which the guardduty events notifications are sent


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

