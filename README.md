# Kubernetes on AWS - EKS

## Technologies used:

- Kubernetes, AWS EKS, AWS Fargate, AWS ECR, Eksctl, Linux,  Docker, Jenkins, Linode LKE,  Docker Hub, Java, Maven, Git

## Job 1: Create AWS EKS cluster with a Node Group
#### Job description:

- Configure necessary IAM Roles
- Create VPC with Cloudformation Template for Worker Nodes
- Create EKS cluster (Control Plane Nodes)
- Create Node Group for Worker Nodes and attach to EKS cluster
- Configure Auto-Scaling of worker nodes
- Deploy a sample application to EKS cluster

## Job 2: Create EKS cluster with Fargate profile
#### Job description:

- Create Fargate IAM Role
- Create Fargate Profile
- Deploy an example application to EKS cluster using Fargate profile

## Job 3: Create EKS cluster with eksctl
#### Job description:

- Create EKS cluster using eksctl tool that reduces the manual effort of creating an EKS cluster

## Job 4: CD - Deploy to EKS cluster from Jenkins Pipeline
#### Job description:

- Install kubectl and aws-iam-authenticator on a Jenkins server
- Create kubeconfig file to connect to EKS cluster and add it on Jenkins server
- Add AWS credentials on Jenkins for AWS account authentication
- Extend and adjust Jenkinsfile of the previous CI/CD
- pipeline to configure connection to EKS cluster

## Job 5: CD - Deploy to LKE cluster from Jenkins Pipeline
#### Job description:

- Create K8s cluster on LKE
- Install kubectl as Jenkins Plugin
- Adjust Jenkinsfile to use Plugin and deploy to LKE cluster

## Job 6: Complete CI/CD Pipeline with EKS and private DockerHub registry
#### Job description:

- Write K8s manifest files for Deployment and Service configuration
- Integrate deploy step in the CI/CD pipeline to deploy newly built application image from DockerHub private registry to the EKS cluster
- So the complete CI/CD projet has the following configuration:
    a. CI step: Increment version
    b. CI step: Build artifact for Java Maven application
    c. CI step: Build and push Docker image to DockerHub
    d. CD step: Deploy new application version to EKS cluster
    e. CD step: Commit the version update

## Job 7: Complete CI/CD Pipeline with EKS and AWS ECR
#### Job description:

- Create private AWS ECR Docker repository
- Adjust Jenkinsfile to build and push Docker Image to AWS ECR
- Integrate deploying to K8s cluster in the CI/CD pipeline from AWS ECR private registry
- So the complete CI/CD project we build has the following configuration:
    a. CI step: Increment version
    b. CI step: Build artifact for Java Maven application
    c. CI step: Build and push Docker image to AWS ECR
    d. CD step: Deploy new application version to EKS cluster
    e. CD step: Commit the version update
