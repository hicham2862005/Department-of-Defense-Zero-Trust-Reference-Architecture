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
focuses on **Securing Applications and Services across all the Network Environments (on-prem or cloud)**, it requires securing:
- Compute Containers
- Virtual Machines (VMs)
- Serverless Functions

and alongside of that it requires the use of **Proxy-based Delivery Methods** for **PDPs** and **PEPs** to achive **Better Isolation and Access Control**,
and with those disscussed above, it uses **DevSecOps Practices** for:

- Developing Secure Source Code
- Inspecting Common Libraries used in the project
- Embedding the Security in the Early stages of the project development

#### Data Pillar:
focuses on **Protecting Mission-critical Data (core assets)** it requires the use of:

- Digital Rights Management (DRM)
- Data Loss Prevenetion (DLP)
- Software-Defined Environments (SDE)
- Granular Data Tagging

also it aims to build a **full data management strategy** that includes:

- Structured Data Igestion
- Data Classification and Schemas
- **Encryption at Rest** and **Encryption at Transit**

#### Visibility and Analytics Pillar:
its main focus are on **understanding what are happening across the environment in the real-time** and alongside with this goal it works on
**Detecting Anomalies and Triggering Alerts based on suspicious events and Adapting policies dynamically for protecting the system** 
and it's also helps in **Monitoring the Behaviour and the Performance also the Security across all othe ZT Pillars**, and for this
various tools and techniques are used such as:
- Contextual Telemetry
- Sensor Data
- Deep Packet Inspection (DPI)

#### Automation and Orchestration Pillar:
this pillar focuses on **High Speed Response and Rules Enforcement** with **Reduction in Human Errors**, it contains
- SOAR (Security Orchestration Automation and Response)
- SIEM Integrations
- Orchestration across **Cloud** and **On-prem**

### ZT Main Principles:
- **P1:** there is **no trusted zones**, all parts of the network are treated like they are compromized
- **P2:** the **Identity-Based Authentication and Authorization** are strictly enforced for **all connections** across the **Infrastructure**,**Services** and **Data Routes**, this includes the use of **Multi-factor Auth (MFA)**, **Public-Key Infrastructure (PKI)** ...
- **P3:** the **Machine-to-Machine (M2M) Authentication** are strictly enforced for **comminucations between Servers and Applications**
- **P4:** the **Risk Profiles** are always generated in **near Real-time** from **Monitoring and Assessment of User/Device Behaviors** and used to **Authorizing User/Device Entities** 
- **P5:** the **Sensitive Data is Always Encrypted** both **At-Rest** and **In-Transit**
- **P6:** **All Events are Continously Monitored, Collected, Stored** and **Analyzed** for **Compliance**, where **all events are logged** and the Logs are **Monitored in Real-time for spotting threats** and also for **Audit Compliance**
- **P7:** both **Policy Management** and **Policy Distribution** are **Centralized** for preventing **Rules Duplication** and **Rule Inconsistencies** and also to **Elemenat Hidden Permissions** that are hard to track
