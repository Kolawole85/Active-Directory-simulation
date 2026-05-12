# Active Directory Simulation – KOLATECH.AI 

This project demonstrates the deployment of a **Windows Server Domain Controller (Active Directory)** for a simulated organization, **KOLATECH.AI**. It covers domain setup, client integration, OU structuring, Group Policy implementation, and access control in an enterprise-like environment.

---

## 🏢 Company Structure

**KOLATECH.AI** is modeled as a small IT services firm with the following setup:

- 1 × Windows Server (Domain Controller)
- 1 × Windows 8 Client PC (Accounts Department)
- 1 × Windows XP Client PC (Legacy System)

---

## 🎯 Project Objectives

- Configure an Active Directory Domain Controller
- Join client machines to the domain
- Design Organizational Units (OUs)
- Implement Group Policies (GPOs)
- Simulate centralized identity and access management

---

## 🌐 Network Design

```
Internet
   ↓
Router (Gateway: 10.0.2.15)
   ↓
Switch
 ┌──────┬─────────────┬──────────────┐
 │      │             │              │
Server  PC1 (Win 8)   PC2 (Win XP)
```

| Device           | IP Address | Role                          |
|------------------|------------|-------------------------------|
| Windows Server   | 10.0.2.15   | Domain Controller (AD DS)     |
| Windows 8 PC     | DHCP       | Client (Accounts Department)  |
| Windows XP PC    | DHCP       | Legacy Client                 |

---

## 🖥️ Domain Configuration

- **Domain Name:** `KOLATECH.AI`
- **Server Name:** `SERVER KOLATECH`
- **IP Address:** `10.0.2.15` (Static)
- **Roles Installed:**
  - Active Directory Domain Services (AD DS)
  - DNS
  - DHCP

---

## 🗂️ Organizational Units (OUs)

Structured using **Active Directory Users and Computers (ADUC):**

```
KOLATECH.AI
├── OU: HR Department
│   ├── IRMIDE
│   └──les.IT Char
│
├── OU: Sales
│   └── Users-Alex jay
```

---

## 🔐 Group Policy (GPO)

Configured via **Group Policy Management Console (gpmc.msc):**

- **GPO Name:** `DisableRemovableDrives`
- **Linked To:** IT Department OU
- **Policy Path:**
  ```
  Computer Configuration → Administrative Templates → System → Removable Storage Access
  ```
- **Setting:**
  - **All Removable Storage Classes: Deny All Access → Enabled**

**Outcome:**  
USB and external storage devices are blocked for users within the targeted OU.

---



- [Active Directory Domain Structure] https://github.com/Kolawole85/Active-Directory-simulation/upload/main/screenshots
- 



---

## 🧠 Key Takeaways

- Hands-on experience deploying and managing Active Directory
- Implementation of centralized access control using GPOs
- Practical OU design aligned with organizational structure
- Real-world application of Identity and Access Management (IAM)

---

## 👤 Author

**Kolawole Olasunkanmi**  
Cybersecurity Analyst
