
## Facebook phishing attack using Zphisher

- **Date: March 29, 2026**

#

**Objective**

The goal of this lab was to perform a realistic Facebook phishing attack using Zphisher on Kali Linux. This exercise demonstrates how attackers create fake login pages to steal user credentials and highlights the importance of verifying URLs before entering any personal information. The lab focuses on understanding the complete workflow of a social engineering phishing attack in a controlled environment.

**Ethical and legal scope**

All activity was carried out in a personal isolated lab environment using test accounts and personal devices. No real users or external accounts were targeted. This lab is strictly for educational and defensive awareness purposes.

**Tools used**

- Kali Linux (latest version)
- Zphisher 2.3.5
- Cloudflared (HTTPS tunneling)
- Firefox browser
- Test Facebook account (Rashad@zmail.com)

**Process**


**Step 1:** Clone & Install Zphisher

**Command used:**
- git clone https://github.com/htr-tech/zphisher.git
- cd zphisher
- chmod +x zphisher.sh

#

**Step 2:** Launch Zphisher

**Command used:**
- ./zphisher.sh

Screenshot:
<img width="1152" height="631" alt="0" src="https://github.com/user-attachments/assets/14e461fc-d9b4-46a5-8bc5-fa42948a44de" />

#

**Step 3:** Select Attack
- I choose option: 1 -> Facebook

Screenshot:
<img width="1156" height="627" alt="1" src="https://github.com/user-attachments/assets/445ee780-7d25-46d3-bd79-de11a4254fbc" />

#

**Step 4:** Choose Login Page Template
- I choose option: 1 -> Traditional Login Page

Screenshot:
<img width="1155" height="628" alt="2" src="https://github.com/user-attachments/assets/38e0f5bd-5e70-450f-a248-fcea5a2d77de" />

#

**Step 5:** Select Port Forwarding Service
- I choose option: 2 -> Cloudflared

Screenshot
<img width="1157" height="623" alt="3" src="https://github.com/user-attachments/assets/7358faef-b99e-4417-924b-c3052c7d6ad2" />

#

**Step 6:** Phishing Link Generated

Screenshot
<img width="1155" height="627" alt="5" src="https://github.com/user-attachments/assets/c06b8c9e-4425-4fc9-8747-1a9316f213f1" />

#

**Step 7:** Send the Phishing Link
- Copy the generated URL and send it to the "victim" (in a controlled lab environment only).
- Example URL from lab: https://angels-cancel-station-poems.trycloudflare.com

#

**Step 8:** Wait for Victim

Screenshot
<img width="1346" height="703" alt="6" src="https://github.com/user-attachments/assets/4eecc831-1e62-45e5-af9b-5d8ace062e62" />
<img width="1912" height="736" alt="7" src="https://github.com/user-attachments/assets/a4a271a6-95b6-4608-93aa-268447d90332" />

#

**Step 9:** Captured Login Information
- Victim IP address (IPv6 in this case)
- Captured Login Information:
  Account: Rashad@zmail.com
  Password: 123456789

- All captured data is automatically saved in:
  auth/ip.txt
  auth/usernames.dat

Screenshot
<img width="1152" height="625" alt="8" src="https://github.com/user-attachments/assets/ca649426-3028-403b-9656-fb1d028fc98b" />

#

**Important Notes from the Lab**

- Zphisher automatically saves all credentials in the auth/ folder.
- Cloudflared provides a free HTTPS tunnel (no port forwarding needed on router).
- The phishing page looks extremely realistic (identical to real Facebook login).
- Victim sees the real Facebook "Save Password" prompt after entering credentials.

**Defensive analysis**

- This lab shows how easily a convincing phishing page can be deployed using automated tools and tunneling services. The cloned page closely resembles the original Facebook login interface, including browser prompts such as "Save Password," which increases its effectiveness against users who do not verify URLs carefully.
- The setup process is fast and requires minimal technical knowledge, which increases the risk of widespread misuse.

**Mitigation**

- Verify the URL before entering credentials. It must match the official domain exactly
- Enable two-factor authentication or passkeys
- Avoid interacting with unsolicited login links
- Use a password manager that restricts autofill to trusted domains
- Check HTTPS certificates when uncertain
- Stay informed about phishing techniques
- Avoid clicking shortened or suspicious links

**Conclusion**

Phishing remains highly effective because it targets user behavior rather than software vulnerabilities. Tools like Zphisher simplify the process of cloning trusted platforms. Strong awareness, careful verification of links, and proper account security measures remain the most reliable defenses.






