# Assignment-2.13

Make a comparison between Serverless Framework and Terraform as tools for IaC. Answer the following:

1. What type of infrastructure and application deployments are each tool best suited for?
2. How do their primary objectives differ?
3. How do they differ in terms of learning curve and ease of use for developers or DevOps teams?
4. What are the differences in how each tool handles state tracking and deployment changes?
5. In what scenarios would you recommend using Serverless Framework over Terraform, and vice versa?
6. Are there scenarios where using both together might be beneficial?

# Answers

1. Serverless framework is best when you need to rapidly deploy serverless applications in microservices and event-driven context. <br>Terraform is for more comprehensive infrastructure management across multiple services and environment. 

2. The primary goal of serverless framework is to simplify the development and deployment of serverless applications enabling developers to quickly build and deploy event-driven functions.
The primary goal of Terraform is for comprehensive infrastructure management with tools for managing a wide array of cloud resources in a consistent and controlled manner.

3. The serverless framework has a lower learning curve for developers as it has a simplified deployment process.
Terraform has a higher learning curve, however it is more powerful and flexible for infrastructure management.

4. The Serverless Framework does not maintain a detailed state file. It relies on the cloud provider infrastructure to keep track of the resources deployed. When deploying changes, it performs incremental updates based on the changes detected in the configuration files. The serverless framework does not have built-in rollback capabilities. If a deployment fails, users may need to manually revert to a previous state.

Terraform uses a state file to keep track of infrastructure resources it manages. Terraform plan would generate an execution plan showing what changes will be made. Terraform apply will then execute these changes. Terraform can handle rollbacks by applying a previous state.

5. Serverless Frameworks is used when the project primarily involved building and deploying serverless applications. It is also used when you need rapid prototyping. If you team consists mainly of developers focus on writing business logic then the serverless frameworks is a good choice.

Terraform is used if the project involved managing a large and complex infrastructure. Terraform is also the choice if your infrastructure spans multiple cloud providers. If the focus is on long-term infrastructure management including the ability to track changes and potentially roll back to a previous state, Terraform is a better choice.

6. When we have a hybrid structure that includes both serverless functions and traditional resources. Using both tools allows us to handle the serverless components using Serverless Frameworks. While Terraform will be used to maintain the whole infrastructure.
