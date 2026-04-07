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
