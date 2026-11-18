# Week 3 – Password Cracking | NetworkWalks Internship

This repository documents my work on **Week 3: Password Cracking** as part of my cybersecurity internship at NetworkWalks.

The project explores two approaches to password recovery using John the Ripper and NetworkWalks' online password-cracking tools.

## Project Objectives

- Understand how password hashes work.
- Learn how password-protected PDF files can be audited.
- Practice password recovery using different tools.
- Understand dictionary-based password cracking.
- Recognize the importance of strong passwords.

---

# Module 1 – Password Cracking with John the Ripper (JTR)

## Overview

For this module, I used **Kali Linux** to perform password recovery on three password-protected PDF files using John the Ripper.

The process involved extracting the password hash from each PDF, saving it into a text file, and using a wordlist attack to attempt password recovery.

## Tools Used

- Kali Linux
- John the Ripper (JTR)
- RockYou Wordlist
- Online Hash Crack – PDF Hash Extractor
- Nano Text Editor

## Step-by-Step Implementation

### Step 1 – Extracting the PDF Hash

I used the Online Hash Crack PDF Hash Extractor to extract the password hash from the protected PDF file.

Website: https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php

![PDF Hash Extraction](step1.1.png)
![PDF ](step1.2.png)

### Step 2 – Creating the Hash File

I created a text file using Nano in the Kali Linux terminal:

```bash
nano hash.txt
```

![Creating Hash File](step1.3.png)

### Step 3 – Saving the Extracted Hash

I copied the extracted hash and pasted it into `hash.txt`, then saved the file.

![Hash Saved](step1.4.png)

### Step 4 – Running John the Ripper

I used the RockYou wordlist to perform a dictionary attack:

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```

John the Ripper tested password candidates from the wordlist against the extracted hash.

![John the Ripper Execution](step1.5.png)

### Step 5 – Displaying the Recovered Password

After the cracking process, I used the following command to display the recovered password:

```bash
john --show hash.txt
```

![Recovered Password](step1.6.png)

### Step 6 – Opening the PDF

Finally, I used the recovered password to open the protected PDF file and verify the result.

*The same procedure was repeated for all three PDF files. The results are presented in the final Results section of this repository.*

---

# Module 2 – Password Cracking with NetworkWalks Tools

## Overview

For this module, I used two free online tools provided by NetworkWalks to recover the passwords of the protected PDF files.

The process involved extracting the hash using the Hash Calculator and then submitting it to the Password Cracker to recover the password.

## Tools Used

- NetworkWalks Hash Calculator
- NetworkWalks Password Cracker
- Web Browser

## Step-by-Step Implementation

### Step 1 – Accessing the Hash Calculator

I visited the NetworkWalks Hash Calculator website.

Website: https://networkwalks.com/hash-calculator/
![Hash Calculator](step2.1.png)

### Step 2 – Extracting the PDF Hash

I uploaded the password-protected PDF file to the Hash Calculator and extracted its hash.

![Hash Calculator](step2.2.png)

### Step 3 – Accessing the Password Cracker

I visited the NetworkWalks Password Cracker website.

Website: https://networkwalks.com/password-cracker/
![Hash Calculator](step2.3.png)

### Step 4 – Uploading the Hash

I submitted the extracted hash to the Password Cracker tool.

![Uploading Hash](step2.4.png)

### Step 5 – Starting the Cracking Process

I clicked on **Start Cracking** to begin the password recovery process.

Once the process was completed, the tool displayed the recovered password.

![Password Cracking](step2.5.png)

### Step 6 – Opening the PDF

Finally, I used the recovered password to open the protected PDF file and verify the result.

*The same procedure was repeated for all three PDF files. The results are presented in the final Results section of this repository.*

---

# Results

Both approaches were successfully used to recover the passwords of the three protected PDF files.

| PDF File | John the Ripper | NetworkWalks Tools |
|---|---|---|
| My Locked PDF 1 | Successfully recovered | Successfully recovered |
| My Locked PDF 2 | Successfully recovered | Successfully recovered |
| My Locked PDF 3 | Successfully recovered | Successfully recovered |

## Results Overview

![Successfully Opened PDF](PASS1.png)
![Successfully Opened PDF](PASS2.png)
![Successfully Opened PDF](PASS3.png)

---

# Comparison Between the Two Approaches

| John the Ripper | NetworkWalks Tools |
|---|---|
| Runs locally on Kali Linux | Runs through a web browser |
| Uses command-line instructions | Uses a graphical interface |
| Requires a hash file and a wordlist | Requires uploading the PDF hash |
| Offers different cracking modes and configurations | Provides a simplified password recovery workflow |

## Key Takeaways

Through these two practical modules, I gained hands-on experience with:

- Extracting password hashes from protected PDF files.
- Understanding how password hashes are used in password recovery.
- Performing dictionary attacks using John the Ripper.
- Using online tools for password recovery.
- Comparing command-line and browser-based approaches.
- Understanding the importance of strong passwords.

**Note:** All practical activities were performed on files provided for this authorized cybersecurity training exercise.

## Author

**Doaa Marouane**  
Cybersecurity & Cloud Computing Student
