                                            # ** lambda-ebs_update-cloud watch ** #
 Changing the newly created EBS volume type from gp2 to gp3 with the help of AWS Lambda and tacking EBS logs with CloudWatch

 
Pre-requisite
1. AWS account
2. Common Sense

Step: 1 Create a new Lambda function with the setting below

![Screenshot 2024-02-10 193914](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/c5694dce-a5d5-41ff-93b9-c68d9dddd815)

Step: 2 Modify the permission of the role as below, so that it can modify EBS volume through source code

![Screenshot 2024-02-10 193914](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/531b4c8c-0f79-4586-b62d-2f0a75273908)

Step: 3 Now create a new EBS volume with type gp2.

Step: 4 Now Create a new Cloudwatch rule with the setting below so that we can know the status of EBS volume through the log stored in Cloudwatch

![Screenshot 2024-02-10 194423](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/19ad33e6-7650-4be7-b50e-36d775008890)

![Screenshot 2024-02-10 194612](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/e2d97bdc-ac8c-4567-a79c-2eddcab7dd37)

![Screenshot 2024-02-10 194628](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/2f56b338-43ea-42ed-8cdd-1713da2bea19)

![Screenshot 2024-02-10 194647](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/44420da0-3f4d-44f5-9ef0-40ad1e21882d)

![Screenshot 2024-02-10 194747](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/3530537c-89f4-42ca-a5df-75e71ec7c5e5)

![Screenshot 2024-02-10 194816](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/e0e4ca20-c364-4a23-a286-ce73464095dd)

Step: 5 Through the log Group we can see logs

![Screenshot 2024-02-10 194920](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/3bab6634-4ed9-4789-98ba-7cd9a1448caa)

Step: 6 Write the Python code in Lambda so that the newly created gp2 type volume will automatically converter to gp3 volume.

![Screenshot 2024-02-10 193805](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/2be09fb9-206e-4ad6-8eb1-4910fe320468)

End result will look like this

![Screenshot 2024-02-10 195716](https://github.com/hijackhim/lambda-ebs_update-cloudwatch/assets/105789918/af60e1f0-4bc0-4686-a048-c16e511b5cb1)




