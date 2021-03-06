# HyperParameterTrainingJobDefinition<a name="API_HyperParameterTrainingJobDefinition"></a>

Defines the training jobs launched by a hyperparameter tuning job\.

## Contents<a name="API_HyperParameterTrainingJobDefinition_Contents"></a>

 **AlgorithmSpecification**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-AlgorithmSpecification"></a>
The [HyperParameterAlgorithmSpecification](API_HyperParameterAlgorithmSpecification.md) object that specifies the algorithm to use for the training jobs that the tuning job launches\.  
Type: [HyperParameterAlgorithmSpecification](API_HyperParameterAlgorithmSpecification.md) object  
Required: Yes

 **InputDataConfig**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-InputDataConfig"></a>
An array of [Channel](API_Channel.md) objects that specify the input for the training jobs that the tuning job launches\.  
Type: Array of [Channel](API_Channel.md) objects  
Array Members: Minimum number of 1 item\. Maximum number of 8 items\.  
Required: Yes

 **OutputDataConfig**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-OutputDataConfig"></a>
Specifies the path to the Amazon S3 bucket where you store model artifacts from the training jobs that the tuning job launches\.  
Type: [OutputDataConfig](API_OutputDataConfig.md) object  
Required: Yes

 **ResourceConfig**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-ResourceConfig"></a>
The resources, including the compute instances and storage volumes, to use for the training jobs that the tuning job launches\.  
Storage volumes store model artifacts and incremental states\. Training algorithms might also use storage volumes for scratch space\. If you want Amazon SageMaker to use the storage volume to store the training data, choose `File` as the `TrainingInputMode` in the algorithm specification\. For distributed training algorithms, specify an instance count greater than 1\.  
Type: [ResourceConfig](API_ResourceConfig.md) object  
Required: Yes

 **RoleArn**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-RoleArn"></a>
The Amazon Resource Name \(ARN\) of the IAM role associated with the training jobs that the tuning job launches\.  
Type: String  
Length Constraints: Minimum length of 20\. Maximum length of 2048\.  
Pattern: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$`   
Required: Yes

 **StaticHyperParameters**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-StaticHyperParameters"></a>
Specifies the values of hyperparameters that do not change for the tuning job\.  
Type: String to string map  
Key Length Constraints: Maximum length of 256\.  
Value Length Constraints: Maximum length of 256\.  
Required: No

 **StoppingCondition**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-StoppingCondition"></a>
Sets a maximum duration for the training jobs that the tuning job launches\. Use this parameter to limit model training costs\.   
To stop a job, Amazon SageMaker sends the algorithm the `SIGTERM` signal\. This delays job termination for 120 seconds\. Algorithms might use this 120\-second window to save the model artifacts\.  
When Amazon SageMaker terminates a job because the stopping condition has been met, training algorithms provided by Amazon SageMaker save the intermediate results of the job\.  
Type: [StoppingCondition](API_StoppingCondition.md) object  
Required: Yes

 **VpcConfig**   <a name="SageMaker-Type-HyperParameterTrainingJobDefinition-VpcConfig"></a>
The [VpcConfig](API_VpcConfig.md) object that specifies the VPC that you want the training jobs that this hyperparameter tuning job launches to connect to\. Control access to and from your training container by configuring the VPC\. For more information, see [Protect Training Jobs by Using an Amazon Virtual Private Cloud](train-vpc.md)\.  
Type: [VpcConfig](API_VpcConfig.md) object  
Required: No

## See Also<a name="API_HyperParameterTrainingJobDefinition_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/sagemaker-2017-07-24/HyperParameterTrainingJobDefinition) 
+  [AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/sagemaker-2017-07-24/HyperParameterTrainingJobDefinition) 
+  [AWS SDK for Java](https://docs.aws.amazon.com/goto/SdkForJava/sagemaker-2017-07-24/HyperParameterTrainingJobDefinition) 
+  [AWS SDK for Ruby V2](https://docs.aws.amazon.com/goto/SdkForRubyV2/sagemaker-2017-07-24/HyperParameterTrainingJobDefinition) 