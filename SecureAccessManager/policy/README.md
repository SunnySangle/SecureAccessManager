# 🚀 SecureAccessManager: AWS IAM Policy-Based Access Control for EC2 and EBS

## 🧩 Project Overview
**SecureAccessManager** demonstrates the AWS security principle **"Allow Broadly, Deny Specifically"** using **IAM Policies** and **Resource Tagging**.  

This project shows how to grant users general EC2 permissions while explicitly denying critical actions (like stopping or terminating production-tagged instances). It ensures that **production resources remain secure**, while developers can still manage non-production environments.

---

## 🧠 Learning Objective
This project is designed to:
- Understand IAM policy structure (`Effect`, `Action`, `Resource`, `Condition`)
- Implement the **Least Privilege Model** using AWS IAM
- Apply **tag-based access control** for EC2 and EBS
- Practice **real-world AWS governance** scenarios

---

## 🧱 Architecture Diagram




*(You can replace this with an uploaded diagram image later)*  
**📸 Screenshot Placeholder:** `![Architecture Diagram](screenshots/architecture-diagram.png)`

---

## 🛠️ AWS Services Used

| Service | Purpose |
|----------|----------|
| **IAM (Identity and Access Management)** | Create users, groups, and custom policies |
| **EC2 (Elastic Compute Cloud)** | Launch and tag instances (`Environment=Production/Development`) |
| **EBS (Elastic Block Store)** | Manage attached storage volumes |
| **AWS CLI / Console** | Configure and test permissions |

---

## ⚙️ Project Setup

### 1️⃣ Step 1: Create IAM User and Group
- Go to **IAM → Users → Add User**
- Choose **Programmatic access** and **Console access**
- Create a **Group** named `Developers`
- Attach only the basic `AmazonEC2FullAccess` policy (temporary)

---

### 2️⃣ Step 2: Create and Attach Custom IAM Policy

Create a new **Inline Policy** and paste the following JSON:

