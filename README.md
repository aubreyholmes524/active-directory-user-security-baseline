# Active Directory User Security Baseline (Windows Server 2022)

## Overview
This project demonstrates the design, implementation, and verification of a basic Active Directory user security baseline using Windows Server 2022. The lab focuses on proper Organizational Unit (OU) design, role-based access control, Group Policy application, and validation of policy enforcement.

The goal of this lab was to simulate a small enterprise Active Directory environment using real-world administrative best practices rather than default configurations.

---

## Environment
- Windows Server 2022
- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- VMware Workstation (virtualized lab environment)

**Domain:**  
`apex.local`

---

## Architecture & Design Decisions

### Organizational Unit (OU) Structure
The domain was designed with custom Organizational Units to separate administrative scope and enable clean policy application:

- **Apex-Admins** – Privileged administrative accounts
- **Apex-Users** – Standard user accounts
- **Apex-Groups** – Security groups for role-based access
- **Apex-Computers** – Domain-joined client systems
- **Apex-Servers** – Server objects

This structure prevents policy sprawl, improves delegation, and mirrors enterprise Active Directory best practices.

---

## Verification & Validation

Group Policy application was verified using native Windows tooling.

Command executed:
gpresult /r /scope:user

The output confirmed that the APEX – User Security Baseline GPO was applied only to users located within the Apex-Users OU and did not affect administrative accounts.

This validated:
- Correct OU scoping
- Proper GPO linking
- Effective role separation between users and administrators
