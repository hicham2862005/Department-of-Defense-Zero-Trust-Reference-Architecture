# Chapter 1 : Introduction
## What is 'Zero Trust' ?
**Zero Trust (ZT):** is a modern Cybersecurity paradigm thats shifts away from **Perimeter-Based Security** (Everything inside the network
are trusted and only what resides ouside of it are considered untrusted), to the concept of **trust evaluation** of the **Users**, **Assets**
 and **Resources** (meaning all of those listed before always verified and validated and not considered trusted by default)


## ZT Terms and Definitions:
### Policy Decision Point (PDP):
Is a component used to **Evaluate Access Requests** and based on the evaluation result, **Authorization Policies** such as
**Allow and Deny** are generated and **sent to Policy Enforcement Points (PEPs)** to be applied

### Policy Enforcement Point (PEP):
Is a component that **works with the PDP**, its main job are **enforcing the Policies recived from the PDP** on the target resource
 that the **PEP** are installed in

### Core ZT Concepts:
* **No more \"Trusted\" and \"Untrusted\" Zones**: everything are considered **Untrusted** by default and must earn trust continouslly
* **Multipale Attributes are used:** the ZTA uses mutipale attributes such as **Identity**, **Location**, **Device Health** ... for things like **Authentication & Authorization** and for **Enforcing Least-Privilege Access**
* **The compromisation are always assumed:** the ZTA always assumes the compromisation both Devices and Software used within the Network, and also assumes the existance of Insiders who have access to sensitive data

### Core ZT Goals:
ZT focuses on protecting **Data**, **Applications**, **Assest** and **Services** (also called **DAAS**), and for that it uses technologies and techniques such as:
* **Continuous MFA (Multi-Factor Auth)**
* **Micro-segmentation**
* **Encryption**
* **Endpoint security**
* **Automation and Analytics**
* **Robust auditing and logging**

### Zero Trust Pillars:
A **Pillar** is a **Key focus area for implementing Zero Trust controls**, Each pillar targets a specific domain (identity, devices ...) and they
there are **two categories of pillars:**
1. **Data Pillar:** which is the **core assest we aim to protect**
2. **Protection Pillars:** are the pillars used to **enforce controls** and for **protecting the core assests (which is the Data Pillar)**, they
include:
    - Devices Pillar
    - Workloads Pillar
    - Visibility and Analytics Pillar
    - Users Pillar
    - Network Pillar (also called Environment Pillar)
    - Automation and Orchestration Pillar
\
\
\
![Figure 1: ZT Pillars](/resources/ZT_pillars.png)

#### User Pillar:
The **User Pillar** works with **Person and Non-person (bots, scripts) entities**, it uses **Multi-Factor Auth (MFA)** and **Privileged Access Management (PAM)**
and requires the use of **Continous Authentication and Authorization** alongside with **Continouse Monitoring**, here the access are governed
based on **Behavoral Patterns** such as **Location**, **Access Patterns** ..., and it focuses on **enforin Least Privilege Access**

#### Devices Pillar:
focuses on the **Trustworthiness** of the **devices that access the network**, it uses techniques such as **Mobile Device Managers (MDM)**,
**Comply-to-Connect (C2C)** and **Trusted Platform Modules (TPM)**, and it requires **Real-time device inspection and Health Checking**, also
it evaluates:
- Software Versions
- Patch Status
- Compromise Indicators
- Encryption Usage
- Config Correctness
also this pillar controls **Device Inventory Isolation and Remediation**

#### Network/Environment Pillar:
it focuses on **Securing the Segmentation of the Network**, it uses **Macro-Segmentation** (Big Zones) and **Micro-Segmentation** (fine-grained Zones),
it requires **Logical and Physical Network Isolation** and **Granular Policies** to control:
- Internal and External data flows
- Leteral Movement through the network
- Priviliged Network Access

#### Workloads Pillar:

#### Data Pillar:

#### Visibility and Analytics Pillar:
