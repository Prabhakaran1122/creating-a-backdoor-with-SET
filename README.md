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
<img width="383" height="249" alt="image" src="https://github.com/user-attachments/assets/e64735dd-efb0-4bed-a690-6e4153d00335" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="507" height="277" alt="image" src="https://github.com/user-attachments/assets/191ff6f4-393f-4b35-a004-c146ee790b9e" />
<img width="745" height="447" alt="image" src="https://github.com/user-attachments/assets/286816b5-ce4d-4c8a-9a98-77c65eba4dd6" />
<img width="636" height="303" alt="image" src="https://github.com/user-attachments/assets/fd746a0c-c9cc-4d26-adbc-7154dc152bf3" />

**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="714" height="136" alt="image" src="https://github.com/user-attachments/assets/db8cd955-655e-4c99-94dc-0171483dda78" />


**6. Send the generated link to the victim.**
<img width="948" height="1126" alt="image" src="https://github.com/user-attachments/assets/300b0940-87e3-464a-bdaa-bd3704700c98" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="1843" height="992" alt="image" src="https://github.com/user-attachments/assets/3276a681-c057-441a-905b-9dd009a46d6b" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
