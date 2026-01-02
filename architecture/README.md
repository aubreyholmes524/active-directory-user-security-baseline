# Architecture Overview

This folder documents the logical architecture of the Active Directory lab environment.

## Domain Information
- **Domain Name:** apex.local
- **Domain Controller:** APEX-DC01
- **OS:** Windows Server 2022
- **Virtualization:** VMware Workstation

## Organizational Unit (OU) Structure
The domain is organized using role-based Organizational Units to support delegation,
security boundaries, and Group Policy targeting.

### Top-Level OUs
- **Apex-Admins** – Administrative user accounts
- **Apex-Users** – Standard domain users
- **Apex-Groups** – Security groups for role-based access
- **Apex-Computers** – Domain-joined client systems
- **Apex-Servers** – Server objects

## Design Rationale
- Separates administrative and standard users
- Enables scoped Group Policy application
- Aligns with enterprise Active Directory best practices
- Simplifies future scaling and delegation

See screenshots in the `screenshots/` directory for visual confirmation.
