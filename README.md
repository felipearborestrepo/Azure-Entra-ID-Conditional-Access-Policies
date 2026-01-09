# 🔐 Microsoft Entra ID Conditional Access Policy Creation

<img width="1536" height="1024" alt="ChatGPT Image Jan 9, 2026, 04_36_18 PM" src="https://github.com/user-attachments/assets/92f7b055-f7e2-4544-9476-a35f5a0ae3b7" />

## 📘 Overview

This project documents a hands-on **Identity & Access Management (IAM)** security lab built in **Microsoft Entra ID (Azure Active Directory)**.  
The lab simulates a real enterprise identity-protection scenario by implementing:

- A **Break-Glass Global Administrator account**
- **Conditional Access policies**
- **Tenant-wide MFA enforcement**
- **Protection of all cloud applications**
- **Microsoft-managed security baselines**

The objective was to design, deploy, and validate modern cloud identity security controls used by enterprise IAM teams.

---

## 🎯 Objectives

- Create a secure Conditional Access architecture  
- Build and configure an emergency **break-glass** account  
- Assign **Global Administrator** privileges properly  
- Enforce **Multi-Factor Authentication (MFA)**  
- Protect **all cloud applications**  
- Prevent tenant lockout  
- Validate Conditional Access protections  

---

## 🏗️ Environment

- **Platform:** Microsoft Azure  
- **Identity Provider:** Microsoft Entra ID  
- **License:** Entra ID P1  
- **Security Controls:** Conditional Access, RBAC, MFA  
- **Authentication:** Microsoft Authenticator  

---

# ✅ Step-by-Step Implementation

---

## 1️⃣ Review Conditional Access Environment

Path:  
Azure Portal → Microsoft Entra ID → Conditional Access → Policies

Confirmed Conditional Access features were available and reviewed Microsoft-managed security policies.

📸 Screenshot: Conditional Access policies overview  

![maxresdefault](https://github.com/user-attachments/assets/3d2d938c-aa61-4cb3-a56d-2917484fba76)

---

## 2️⃣ Create Break-Glass Emergency Account

Created a dedicated emergency administrator account to prevent tenant lockout.

User created:
- **breakglass.admin**
- Display name: **Break Glass Administrator**

Steps:
1. Microsoft Entra ID → Users  
2. New user → Create new user  
3. Enter username, display name, strong password  
4. Review + Create  

📸 Screenshot: Break-glass user creation  

<img width="406" height="192" alt="Screenshot 2026-01-09 145712" src="https://github.com/user-attachments/assets/88581c93-044e-46e5-9d0e-cfba320114dd" />

<img width="727" height="587" alt="Screenshot 2026-01-09 145818" src="https://github.com/user-attachments/assets/d4100649-0bca-416e-bad0-a4c256a251c5" />

---

## 3️⃣ Assign Global Administrator Role

Granted full emergency privileges to the break-glass account.

Steps:
1. Microsoft Entra ID → Roles and administrators  
2. Search **Global Administrator**  
3. Open role → Add assignments  
4. Assign **Break Glass Administrator**

📸 Screenshot: Global Administrator role  

<img width="1024" height="481" alt="Screenshot 2026-01-09 145846" src="https://github.com/user-attachments/assets/3e2bc366-dcf7-4e18-b684-b378778d2904" />

📸 Screenshot: Break-glass assigned  

<img width="527" height="225" alt="Screenshot 2026-01-09 145912" src="https://github.com/user-attachments/assets/da543693-5803-4dcc-86a6-76e9d7dee3fa" />

<img width="787" height="401" alt="Screenshot 2026-01-09 145943" src="https://github.com/user-attachments/assets/586583ab-80b0-426d-a953-750f47ec7882" />

---

## 4️⃣ Create Conditional Access Policy (Require MFA)

<img width="453" height="206" alt="Screenshot 2026-01-09 150015" src="https://github.com/user-attachments/assets/11c883b2-8f26-4c0a-81d2-5086a0781c98" />

Created a new Conditional Access policy:

Policy Name:  
`CA – Require MFA for All Users`

Configuration:
- Users: **All users**
- Exclusions: **Break Glass Administrator**

📸 Screenshot: All users selected  

<img width="682" height="447" alt="Screenshot 2026-01-09 151253" src="https://github.com/user-attachments/assets/867e6c41-2136-442c-86e6-bdd255cce4a8" />

📸 Screenshot: Break-glass excluded  

<img width="747" height="550" alt="Screenshot 2026-01-09 151314" src="https://github.com/user-attachments/assets/47a91a00-6226-4707-a355-3387502ece5b" />

---

## 5️⃣ Protect All Cloud Applications

Configured the policy to apply to:

✔ **All resources (formerly “All cloud apps”)**

📸 Screenshot: All cloud apps selected  

<img width="637" height="421" alt="Screenshot 2026-01-09 151352" src="https://github.com/user-attachments/assets/c29f6cc7-2a3c-427a-b7e7-150c34d5d90a" />

---

## 6️⃣ Configure Grant Controls

Access control set to:

✔ Grant access  
✔ Require multi-factor authentication  

📸 Screenshot: Grant control – Require MFA  

<img width="300" height="546" alt="Screenshot 2026-01-09 151429" src="https://github.com/user-attachments/assets/b1a46339-317b-4c8c-9d2c-05d041a88108" />

---

## 7️⃣ Enable and Enforce Policy

Policy was enabled and enforced.

Acknowledged system warning and confirmed enforcement.

📸 Screenshot: Policy enabled  

<img width="1315" height="596" alt="Screenshot 2026-01-09 151509" src="https://github.com/user-attachments/assets/b5ba1a88-0a1f-4c14-ab3a-9fb0a69ce166" />

---

## 8️⃣ Verify Tenant Protection

Reviewed Conditional Access policies.

Microsoft-managed policies active:
- Block legacy authentication  
- MFA for Azure management  
- MFA for admins  
- MFA for all users  

📸 Screenshot: Active policies  

<img width="1345" height="608" alt="Screenshot 2026-01-09 151529" src="https://github.com/user-attachments/assets/a76e7cc3-1b1d-4512-a3bf-a6a044f1cc17" />

---

# 🧪 What This Lab Demonstrates

- Enterprise Conditional Access design  
- MFA enforcement across a tenant  
- Break-glass emergency access planning  
- Global Administrator role assignment  
- Cloud application protection  
- Identity security hardening  

---

# 🛠️ Tools & Technologies

- Microsoft Azure Portal  
- Microsoft Entra ID  
- Conditional Access  
- Microsoft Authenticator  
- Azure RBAC  
- Entra ID P1 Security Features  

---

# 🧠 Skills Demonstrated

- Identity & Access Management (IAM)  
- Conditional Access policy creation  
- Privileged account protection  
- Break-glass account design  
- Cloud identity security  
- Authentication enforcement  
- Enterprise documentation  

---

# 🚀 Future Improvements

- Privileged Identity Management (PIM)  
- Risk-based Conditional Access  
- Device compliance enforcement  
- Location-based access rules  
- Microsoft Sentinel sign-in monitoring  
- CyberArk PAM labs  

---

## 👤 Author

**Felipe Restrepo**  
Cybersecurity | IAM | Cloud Security  

---

## ⚠️ Notes

All screenshots in this repository document the real configuration process.  
Sensitive information has been redacted.

---

# 📂 Repository Structure (recommended)
