### Project Title - Deploy a high-availability web app using CloudFormation
This folder provides the starter code for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:


#### final-project-starter.yml
Students have to write the CloudFormation code using this YAML template for building the cloud infrastructure, as required for the project. 

#### server-parameters.json
Students may use a JSON file for increasing the generic nature of the YAML code. For example, the JSON file contains a "ParameterKey" as "EnvironmentName" and "ParameterValue" as "UdacityProject". 

In YAML code, the `${EnvironmentName}` would be substituted with `UdacityProject` accordingly.

  # instace profile contains the IAM Role name(s) that we want to associate to our auto scaling EC2 Servers
  # never give too much permissions to your EC2 instances! if they get hacked, the permissions get hacked also!
  # in this example, I create a Role called UdacityS3ReadOnlyC2 and just give it a policy of S3 Read-Only Access
  ProfileWithRolesForOurApp:
    Type: AWS::IAM::InstanceProfile
    Properties:
      Roles:
        - UdacityS3ReadOnlyEC2