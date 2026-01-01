# AWS IAM & CLI Configuration Project

## 🚀 Project Overview
This project documents my hands-on practice with **AWS Identity and Access Management (IAM)** and the **AWS Command Line Interface (CLI)**. The goal was to secure the AWS account and configure programmatic access.

## 🛠️ Technologies & Tools
* **AWS Services:** IAM (Users, Groups, Policies, MFA)
* **Tools:** AWS CLI v2, Windows PowerShell / Terminal
* **Environment:** AWS Free Tier

## 📋 Key Implementations

### 1. Identity and Access Management (IAM)
* **Root Account Security:** Enabled MFA (Multi-Factor Authentication) for the root user to secure the account.
* **User Management:** Created individual IAM users to avoid using the root account for daily tasks.
* **Groups & Policies:**
    * Created groups (e.g., `Admins`, `Developers`).
    * Attached managed policies (e.g., `AdministratorAccess`) to groups.
    * Simulated permission boundaries using custom policies.
* **Security Best Practices:** Enforced strong password policies and rotated access keys.
* **IAM Roles:**
    * Created roles for AWS Services (e.g., EC2) to access S3 buckets securely.
    * Eliminated the need for hard-coding access keys inside the application code.
  
### 2. AWS CLI Setup
* Installed AWS CLI on Windows.
* Configured credentials using `aws configure`.
* Verified installation and connectivity:
    ```bash
    aws --version
    aws iam list-users
    ```
### 3. Security Audit & Best Practices
* **IAM Credentials Report:** Generated reports to audit all users' status, MFA usage, and access key rotation cycles.
* **IAM Access Advisor:** Analyzed service last accessed data to identify and remove unused permissions (Service-level least privilege).
* **Policy Simulator:** Tested IAM policies to verify permissions before attaching them to users/roles.

## 🎯 Learning Outcomes
* Understood the difference between Root User and IAM User.
* Learned how to manage permissions using the Principle of Least Privilege.
* Gained experience in controlling AWS resources via the terminal (CLI) instead of just the console.
