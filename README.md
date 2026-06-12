# Enterprise IAM Home Lab

## Overview

This project demonstrates the design, implementation, and management of an Enterprise Identity and Access Management (IAM) environment using Active Directory Domain Services (AD DS).

The lab was built to simulate real-world IAM operations including user provisioning, role-based access control (RBAC), password management, account lockout controls, identity lifecycle management, access reviews, and security auditing.

---

## Project Objectives

- Deploy Active Directory Domain Services
- Create and manage Organizational Units (OUs)
- Implement Role-Based Access Control (RBAC)
- Configure Password Policies
- Configure Account Lockout Policies
- Implement Joiner-Mover-Leaver (JML) Processes
- Manage Shared Folder Permissions
- Perform Password Reset Operations
- Conduct Access Reviews
- Monitor Security Events using Event Viewer

---

## Lab Environment

### Domain Controller

- Hostname: DC01
- Operating System: Windows Server 2022
- Roles:
  - Active Directory Domain Services (AD DS)
  - DNS
  - Group Policy Management

### Client Machine

- Hostname: Windows10-Enterprise
- Operating System: Windows 10 Enterprise
- Joined Domain: corp.local

### Domain

corp.local

---

## Technologies Used

- VMware Workstation
- Windows Server 2022
- Windows 10 Enterprise
- Active Directory Users and Computers (ADUC)
- Group Policy Management Console (GPMC)
- Event Viewer
- Shared Folders and NTFS Permissions
- Draw.io

---

## Architecture Diagram

[IAM Architecture Diagram](Architecture/IAM-Architecture-Diagram.png)

---

## Active Directory Structure

### Organizational Units

- HR
- Finance
- IT

### Security Groups

- HR_Users
- Finance_Users
- SOC_Analysts

### User Accounts

- Mary.HR
- James.FIN
- John.SOC
- Sarah.HR

---

## RBAC Implementation

Access was assigned using Security Groups rather than directly to users.

### Access Model

| User | Group | Resource |
|--------|---------|----------|
| Mary.HR | HR_Users | HR Share |
| James.FIN | Finance_Users | Finance Share |
| John.SOC | SOC_Analysts | IT Share |
| Sarah.HR | SOC_Analysts | IT Share |

---

## IAM Controls Implemented

### User Provisioning

- User account creation
- Group assignment
- Resource access assignment

### Password Management

- Password complexity requirements
- Password expiration policies

### Account Lockout Protection

- 5 failed logon attempts
- Automatic account lockout
- Security event generation

### Password Reset Workflow

- Administrative password reset
- Forced password change at next logon

### Joiner-Mover-Leaver (JML)

#### Joiner

- New user creation
- Access assignment

#### Mover

- Department transfer
- Access review and modification

#### Leaver

- Account disablement
- Access revocation

### Access Reviews

- Group membership validation
- Access certification review
- Least privilege verification

---

## Security Auditing

The following security events were successfully monitored:

| Event ID | Description |
|-----------|-------------|
| 4624 | Successful Logon |
| 4634 | Logoff |
| 4740 | Account Lockout |

---

## Project Documentation

Detailed documentation can be found in the Documentation folder:

- Environment Setup
- Active Directory Configuration
- RBAC Implementation
- Password Policy
- Account Lockout Policy
- Shared Folder Permissions
- Password Reset Workflow
- Joiner-Mover-Leaver Lifecycle
- Event Monitoring
- Access Reviews

---

## Key Skills Demonstrated

- Identity and Access Management (IAM)
- Active Directory Administration
- Role-Based Access Control (RBAC)
- Identity Lifecycle Management
- Access Governance
- Security Auditing
- User Provisioning and Deprovisioning
- Group Policy Management
- Windows Security Administration

---

## Lessons Learned

This project provided hands-on experience with:

- Enterprise IAM concepts
- Active Directory administration
- Security group management
- Access governance
- Identity lifecycle management
- Security event monitoring
- Troubleshooting authentication and access issues

---

## Future Improvements

- Azure AD / Microsoft Entra ID Integration
- Hybrid Identity Configuration
- Privileged Access Management (PAM)
- Multi-Factor Authentication (MFA)
- PowerShell Automation
- Access Request Workflows

---
