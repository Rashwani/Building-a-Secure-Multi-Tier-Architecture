# Secure Multi-Tier Application with AWS

This project demonstrates the development of a **Secure Multi-Tier Application** using a variety of AWS services. The application architecture ensures high security, scalability, and availability by separating the application into different tiers and securing each layer with AWS best practices.

## Project Overview

In this project, I built a secure multi-tier architecture that separates the web, application, and database layers, ensuring better security and manageability. The architecture incorporates several security measures such as **SSL**, **WAF**, and **AWS KMS** to safeguard data and communications across the infrastructure.

You can view the project details [here](https://awsportfolio.sila.studio/project/secure-multi-tier-application/).

This project was part of the **Digital Cloud Training** bootcamp, where I gained practical experience in creating secure and scalable applications using AWS services.

### Key Features
- **Multi-Tier Architecture**: Divided into three tiers:
  1. **Web Tier**: Handled by **Amazon CloudFront** and **Elastic Load Balancing (ALB)**.
  2. **Application Tier**: Hosted on **EC2** instances in a private subnet.
  3. **Database Tier**: Managed by **Amazon RDS** in a private subnet.
- **Web Application Firewall (WAF)**: Configured to protect against common web attacks.
- **SSL/TLS Encryption**: Implemented to ensure secure data transmission.
- **AWS Config and Inspector**: Used for continuous monitoring and auditing of AWS resources.
- **Secrets Management**: Secured sensitive information like database credentials using **AWS Secrets Manager**.
- **Data Encryption**: Protected data at rest using **AWS KMS** (Key Management Service).

## Architecture

The solution includes:
1. **Amazon CloudFront**: Distributes content globally, acting as a CDN with SSL termination.
2. **Elastic Load Balancer (ALB)**: Balances incoming traffic across multiple EC2 instances in the application tier.
3. **Amazon EC2**: Hosts the application layer in a private subnet for added security.
4. **Amazon RDS**: Manages the database in a private subnet, accessible only from the application layer.
5. **AWS WAF**: Protects the application from common security threats.
6. **AWS Config**: Continuously monitors AWS resources for compliance and security vulnerabilities.
7. **AWS Secrets Manager**: Manages credentials and secrets securely across the tiers.
8. **AWS KMS**: Encrypts data both in transit and at rest.

![Architecture Diagram]

## AWS Services Used
- **Amazon CloudFront**: For global content delivery and SSL termination.
- **Elastic Load Balancer**: For distributing traffic across EC2 instances.
- **Amazon EC2**: For hosting the application in a secure, private environment.
- **Amazon RDS**: For managing the relational database securely in the private subnet.
- **AWS WAF**: For protection against web attacks.
- **AWS Config & Inspector**: For auditing and monitoring the AWS environment.
- **AWS KMS**: For encrypting data at rest.
- **AWS Secrets Manager**: For securely managing database credentials and other sensitive data.

## How to Deploy
1. Clone the repository to your local environment.
2. Deploy the infrastructure using AWS CloudFormation.
3. Set up SSL certificates in **AWS Certificate Manager (ACM)** and configure the ALB to use them.
4. Configure **WAF** rules to protect against common web vulnerabilities.
5. Launch the application and monitor security using AWS Config and Inspector.

## Lessons Learned
- Designing a multi-tier application architecture improves security and scalability by isolating different layers.
- Implementing AWS WAF and SSL encryption ensures protection against common security threats.
- Continuous monitoring with AWS Config and Inspector is key to maintaining a secure infrastructure.

## Next Steps
- Integrate **AWS Lambda** for automated security monitoring and alerts.
- Add **Auto Scaling** to dynamically adjust the number of EC2 instances based on traffic.
- Explore additional encryption mechanisms for further data security.

## Acknowledgments

This project was completed as part of the **Digital Cloud Training** bootcamp.

## Conclusion

This project showcases how to build a highly secure, scalable, and resilient multi-tier application using AWS services. By implementing industry-standard security practices, this architecture ensures robust protection and compliance with security policies.
![Screenshot 2024-03-11 155057](https://github.com/user-attachments/assets/d074fa3b-0bdd-4b0b-a6bd-2928b2edec46)
