# cfnresponse

This package contains the Amazon Web Services (AWS) cfnresponse module which is
available in Python AWS Lambda environments.

The code for this module can be found [in the Lambda Function Code documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html#cfn-lambda-function-code-cfnresponsemodule)
and in the [awslabs GitHub repo](https://github.com/awslabs/aws-cloudformation-templates/blob/master/aws/services/CloudFormation/MacrosExamples/StackMetrics/lambda/cfnresponse.py)

You can compare the code in `awslabs` with this pypi package with this command

```
if [ "$(curl -s https://raw.githubusercontent.com/awslabs/aws-cloudformation-templates/master/aws/services/CloudFormation/MacrosExamples/StackMetrics/lambda/cfnresponse.py | sha256sum)" = "$(curl -s https://raw.githubusercontent.com/gene1wood/cfnresponse/master/cfnresponse/__init__.py | sha256sum)" ]; then echo "Files match"; fi
```

The [`setup.py`](setup.py) for this module depends on a version of 
[`botocore`](https://github.com/boto/botocore) prior to 
[`1.13.0`](https://github.com/boto/botocore/releases/tag/1.13.0)
when [`botocore.vendored.requests` was removed](https://github.com/boto/botocore/pull/1829)
which would break `cfnresponse`.