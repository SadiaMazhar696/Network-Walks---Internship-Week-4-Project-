# Network-Walks---Internship-Week-4-Project
# Mediroza Hospital: Web Application Penetration Test
Password Cracking & Web Exploitation Lab Documentation

Welcome to my documentation for the Cybersecurity Internship Project (Week 4) of Network Walks. In this module, I performed a comprehensive web application penetration test on a simulated healthcare portal. The assessment covered initial access via web vulnerabilities, extraction of confidential data, hash extraction, password cracking, and identifying critical exposed backups.

🛠️ Lab Overview & Objectives
Bypass the Patient Portal authentication mechanism.

Extract and download confidential patient laboratory reports (PDFs).

Configure John the Ripper and use Network Walks Online tools to crack encrypted PDF hashes.

Discover exposed directory listings and extract sensitive database backup files.

Document findings professionally for the final Pentest Report (M4).

📂 Step-by-Step Implementation & Screenshots
##   Part 1: Initial Access & Web Exploitation (M1)
First, I performed reconnaissance on the Patient Portal login page. By analyzing the web application's response to specific inputs, I identified an SQL Injection vulnerability. I successfully bypassed the authentication mechanism without valid credentials to gain access to the dashboard.

Patient Portal Login & SQL Injection Discovery:
<img width="1365" height="682" alt="or&#39;1=1&#39; error sql 13 ss" src="https://github.com/user-attachments/assets/780be0af-cd47-4af2-a7c3-392f767a98d3" />

Directory Listing Discovery:
<img width="1338" height="726" alt="patient" src="https://github.com/user-attachments/assets/4552430a-6df1-416c-8611-5ad9bb87038a" />

Patient Dashboard Access Gained:
<img width="1364" height="725" alt="my lab reports" src="https://github.com/user-attachments/assets/02955ba8-6f4c-4014-873d-9ee01fe40fa7" />

##   Part 2: Hash Extraction & PDF Password Cracking (M2)
Next, I utilized Network Walks' Hash Calculator to extract the hash from the downloaded encrypted PDF files. After obtaining the hashes, I used both the Network Walks Password Cracker and the command-line tool John the Ripper on Kali Linux to perform dictionary attacks.

Hash Calculator Interface:
<img width="1476" height="1107" alt="file" src="https://github.com/user-attachments/assets/86b727be-7ca3-4e81-8642-303e722c85c7" />

Hash Extraction using Kali Linux Terminal:
<img width="1107" height="1476" alt="file (1)" src="https://github.com/user-attachments/assets/eb4458c3-6e1b-47ec-834f-c86bd9afb7c2" />

Password Successfully Cracked (John the Ripper):
<img width="1365" height="720" alt="report 3 password cracked" src="https://github.com/user-attachments/assets/57fa8064-40cb-435d-a433-700095872d95" />

Decrypted Patient Lab Reports:
# Report 1
<img width="1365" height="767" alt="report 1 ss" src="https://github.com/user-attachments/assets/2bfec44b-5e80-42ef-9ef7-740a49e3b85f" />

# Report 2
<img width="1365" height="728" alt="report 2 ss" src="https://github.com/user-attachments/assets/f75d1d22-c625-42c3-8469-418b664c7665" />

# Report 3
<img width="1365" height="767" alt="report 3 ss" src="https://github.com/user-attachments/assets/6d9dc78e-473f-4aa2-9b89-6cb07fc25e69" />

##   Part 3: Sensitive Data Exposure & Database Extraction (M3)
During the information gathering phase, I analyzed the robots.txt file and discovered hidden directories that were not meant to be public. By exploring these misconfigured directories (Directory Listing), I found an exposed SQL database backup file. This allowed me to extract sensitive corporate data, including employee salaries and shareholder information.

Analysis of robots.txt:
<img width="1363" height="727" alt="ss8 robot txt reconnaissance " src="https://github.com/user-attachments/assets/d7cac151-a5c2-48d3-b2cd-ac125d5c7283" />

Exposed Directory Listing:
<img width="1365" height="725" alt="patient directory" src="https://github.com/user-attachments/assets/d54c7ad3-9d61-4dcc-a496-b9990eb72084" />

SQL Backup File - Staff Salaries & Shareholder Data:
<img width="1364" height="726" alt="ss 9 staff record m3 " src="https://github.com/user-attachments/assets/72610569-30e9-47c0-9ecc-ac82fb45fd04" />
<img width="1365" height="728" alt="ss10 shareholder record m3" src="https://github.com/user-attachments/assets/f7017d94-c4b6-42f6-8f66-abaaa705cb72" />


📝 Conclusion
This lab provided hands-on experience in identifying critical web vulnerabilities and understanding the severe impact of weak document encryption and exposed server files. It highlighted the importance of secure coding practices (preventing SQLi) and proper server configuration (disabling directory listing). All findings were documented in a detailed professional penetration testing report.

Status: Completed Successfully ✅

Author: Sadia Mazhar | Cybersecurity Intern |NetworkWalks
