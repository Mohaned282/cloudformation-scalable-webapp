**Scalable Web Application Deployment with AWS CloudFormation**

This project automates the deployment of a highly available and scalable web application infrastructure on AWS using CloudFormation templates. By leveraging an Application Load Balancer (ALB), Auto Scaling Groups, and EC2 instances, it provides a fault-tolerant, cost-efficient solution for hosting dynamic web applications.

**Overview**

Modern applications require reliability, scalability, and security to support dynamic workloads. This project delivers a streamlined, automated approach to deploy a production-ready infrastructure with minimal manual effort.

**Architecture Diagram**

Below is a high-level view of the architecture:

**Key Components:**

- **Application Load Balancer (ALB):** Manages incoming HTTP traffic and evenly distributes it across EC2 instances.
- **Auto Scaling Group (ASG):** Dynamically adjusts the number of EC2 instances to meet traffic demands.
- **Launch Configuration:** Pre-configures EC2 instances with necessary software (HTTPD and PHP).
- **Security Groups:** Enforce strict traffic flow between ALB, EC2, and external sources.
- **CloudFormation Template:** Automates the deployment of all resources.

**Objectives**

- Deploy a PHP-based web application using a fault-tolerant and scalable architecture.
- Automate infrastructure provisioning with AWS CloudFormation.
- Ensure secure, efficient, and cost-effective resource utilization.

**Features**

- **Automation:** One-click deployment using CloudFormation templates.
- **Scalability:** Auto Scaling Groups adjust EC2 instances to handle variable traffic loads.
- **Security:** Strict ingress rules ensure secure communication between ALB and EC2.
- **Flexibility:** Easily customizable template for additional use cases or regions.

**Deployment Steps**

**Prerequisites**

- An AWS account with appropriate permissions.
- A valid Amazon EC2 Key Pair.
- Pre-existing VPC and subnet IDs.

**Instructions**

1. **Clone the repository:**

- git clone <https://github.com/Mohaned282/cloudformation-scalable-webapp.git>
- cd cloudformation-project.yaml

1. **Deploy the CloudFormation stack:**

- aws cloudformation deploy \\
- \--template-file cloudformation-template.yaml \\
- \--stack-name scalable-web-app \\
- \--parameter-overrides \\
- myKeyPair=your-key-name \\
- VpcId=your-vpc-id \\
- SubnetIds="subnet-1,subnet-2"

1. **Access the application:**

- Retrieve the public DNS of the ALB from the stack outputs and open it in your browser.

**Results and Benefits**

| **Aspect** | **Impact** |
| --- | --- |
| **Scalability** | Handles traffic spikes by dynamically scaling EC2 instances. |
| **High Availability** | Ensures uptime with multiple EC2 instances and an ALB. |
| **Security** | Restricts EC2 traffic to the ALB for enhanced protection. |
| **Cost Optimization** | Minimizes costs by scaling resources based on demand. |
| **Efficiency** | Reduces deployment time to minutes with zero manual errors. |

**Lessons Learned**

- Automation enhances consistency and reduces human error in infrastructure setup.
- Modular design in CloudFormation templates simplifies customization and reusability.
- Security practices, like restricting traffic between resources, improve the system's safety.

**Contribution and Support**

Contributions are welcome! If you have feature suggestions or encounter issues, feel free to:

- Open an issue on GitHub.
- Submit a pull request.

**Author**

**Mohaned**  
Senior Network Engineer with Extensive IT Experience| Aspiring AWS Cloud Architect | Passionate About Cloud Innovation
