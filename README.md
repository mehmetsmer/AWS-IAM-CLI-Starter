# AWS IAM & CLI - Learning Labs

## 📚 About This Repository
This repository serves as a foundational log of my journey into AWS security. It documents the configuration of Identity and Access Management (IAM) and the setup of the AWS Command Line Interface (CLI) based on best practices.

## 🛠️ Technologies & Tools
* **AWS Services:** IAM (Users, Groups, Policies, MFA, Roles)
* **Tools:** AWS CLI v2, Windows PowerShell / Terminal
* **Environment:** AWS Free Tier

## 📋 Key Implementations

### 1. Identity and Access Management (IAM)
* **Root Account Security:** Enabled MFA (Multi-Factor Authentication) for the root user as the first line of defense.
* **User Management:** Created individual IAM users to avoid using the root account for daily tasks.
* **Groups & Policies:**
    * Created functional groups (e.g., `Admins`, `Developers`).
    * Attached managed policies (e.g., `AdministratorAccess`) to groups effectively.
    * Simulated permission boundaries using custom policies.
* **Security Best Practices:** Enforced strong password policies and implemented access key rotation.
* **IAM Roles (Crucial):**
    * Created roles for AWS Services (e.g., EC2) to access S3 buckets securely.
    * **Key Achievement:** Eliminated the need for hard-coding access keys inside application code by utilizing Roles.

### 2. AWS CLI Setup
* Installed AWS CLI on Windows environment.
* Configured credentials securely using `aws configure`.
* Verified installation and connectivity via terminal:
    ```bash
    aws --version
    aws iam list-users
    ```

### 3. Security Audit & Best Practices
* **IAM Credentials Report:** Generated reports to audit user status, MFA usage, and access key rotation cycles.
* **IAM Access Advisor:** Analyzed "service last accessed" data to identify and remove unused permissions (Service-level least privilege).
* **Policy Simulator:** Tested IAM policies to verify permissions before attaching them to live users/roles.

## 🎯 Learning Outcomes
* Understood the critical distinction between Root User and IAM User.
* Learned how to manage permissions using the **Principle of Least Privilege**.
* Gained experience in controlling AWS resources via the terminal (CLI) instead of relying solely on the Management Console.
