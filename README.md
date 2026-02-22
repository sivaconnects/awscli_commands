
---

# 🚀 AWS CLI Configuration & Usage Guide

This repository explains **how to install, configure, and start using AWS CLI** on a Linux machine.

AWS CLI allows you to interact with AWS services directly from the terminal.

---

## 📌 Prerequisites

Before starting, make sure you have:

* An **AWS account**
* An **IAM user** with programmatic access
* A **Linux machine** (Ubuntu / Amazon Linux / CentOS, etc.)

---

## 🧰 Step 1: Install AWS CLI

Install AWS CLI on your Linux machine by following the **official AWS documentation**:

👉 [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

After installation, verify:

```bash
aws --version
```

---

## 🔐 Step 2: Create Access Key & Secret Key

1. Log in to **AWS Console**
2. Go to **IAM**
3. Select **Users**
4. Click on your **user name**
5. Open **Security credentials** tab
6. Under **Access keys**, click **Create access key**
7. Save:

   * **Access Key ID**
   * **Secret Access Key** (important – shown only once)

⚠️ **Never commit these keys to GitHub**

---

## ⚙️ Step 3: Configure AWS CLI

Run the configuration command:

```bash
aws configure
```

You will be prompted to enter:

```text
AWS Access Key ID     : <your-access-key>
AWS Secret Access Key : <your-secret-key>
Default region name   : ap-south-1
Default output format : json
```

---

## ✅ Step 4: Verify Configuration

Check if AWS CLI is properly configured:

```bash
aws --version
```

Optional test:

```bash
aws sts get-caller-identity
```

If this returns your **AWS account ID and user ARN**, the setup is successful 🎉

---

## 🧪 Step 5: Using AWS CLI

You can now start creating and managing AWS resources using AWS CLI.

Example:

```bash
aws ec2 describe-instances
```

For any AWS service or command:

* Refer to **AWS CLI documentation**
* Use built-in help:

```bash
aws help
aws ec2 help
```

---

## 📚 References

* AWS CLI Official Docs
  [https://docs.aws.amazon.com/cli/](https://docs.aws.amazon.com/cli/)

---

## ⚠️ Security Best Practices

* Do NOT share your access keys
* Do NOT push `.aws/credentials` to GitHub
* Use **IAM roles** instead of keys when working on EC2

---

## 🎯 You’re Ready to Go

AWS CLI is now configured on your system.
Start automating AWS resources like a DevOps engineer 🚀

---

