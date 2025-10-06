# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit

```
<img width="360" height="240" alt="image" src="https://github.com/user-attachments/assets/2679f08f-51f9-4dda-be25-f3b77c430b64" />


```
**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```

<img width="691" height="637" alt="image" src="https://github.com/user-attachments/assets/a0f68aad-c98a-4714-9ddf-df3c49c28fe2" />


**4. Choose:**
```bash
2) Site Cloner
```

<img width="463" height="237" alt="image" src="https://github.com/user-attachments/assets/87cde3fe-af45-4172-9d33-5c24d44a0c30" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**

<img width="897" height="207" alt="image" src="https://github.com/user-attachments/assets/1073a559-6138-461a-9b7a-0f89f0a294f0" />



**6. Send the generated link to the victim.**

<img width="745" height="627" alt="image" src="https://github.com/user-attachments/assets/7158af8c-3fea-4e90-8779-90ed2ff9166c" />



**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```

<img width="873" height="400" alt="image" src="https://github.com/user-attachments/assets/72b63029-777e-4e32-82dc-ce9dd9c79dda" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
