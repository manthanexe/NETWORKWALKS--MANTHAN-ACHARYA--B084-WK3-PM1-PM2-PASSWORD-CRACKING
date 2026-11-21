NETWORKWALKS-MANTHAN-B084-WK3-PM1-PM2-PASSWORD-CRACKING
Networkwalks Cybersecurity Internship — Batch B084
Intern: Manthan Acharya
Week 3 — Project Modules 1 & 2 (Essentials)
This repository covers both required Week 3 modules: recovering the password of a protected PDF file using two different methods — John the Ripper (JTR) and the Networkwalks online tools.
WK3-PM1 — Password Cracking with JTR
Task: Crack the password of the attached PDF (⁠My Locked PDF1.pdf⁠) using JTR John and JTR Johnny.
Steps performed:
1. Extracted the PDF's password hash using the Online HashCrack PDF hash extractor tool (⁠$pdf$...⁠ format, compatible with ⁠pdf2john⁠ and ⁠pdf2hashcat⁠), and saved it into ⁠hash1.txt⁠.
2. Opened Johnny (the JTR GUI), configured John the Ripper's executable path (⁠john-1.9.0-jumbo-1-win64⁠), and loaded ⁠hash1.txt⁠ via Open password file.
3. Started the attack. Johnny cracked the password: ⁠good-luck⁠ (⁠100% (1/1: 1 cracked, 0 left)⁠).
4. Confirmed the result by opening the PDF with the recovered password and capturing Flag1: ⁠nw{networkwalks_flag1_jtr_270521_1}⁠.
WK3-PM2 — Password Cracking with Networkwalks Tools
Task: Crack the password of the attached PDF (⁠My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf⁠) using the Networkwalks Hash Calculator and Password Cracker (browser-based, no install required).
Steps performed:
1. Uploaded the locked PDF to the Networkwalks Hash Calculator — it parsed the file locally and returned the ⁠$pdf$...⁠ hash (Revision R4, Version V4, 128-bit key length).
2. Pasted the hash into the Networkwalks Password Cracker and ran a dictionary attack using the built-in 100-word list. The tool cracked the password: ⁠password1⁠ (matched at 91/100).
3. Confirmed the result by opening the PDF with the recovered password and capturing Flag1: ⁠nw{cybersecurity_flag_captured_2608}⁠.
Key takeaway
Both labs recover the same class of password (a PDF user/owner password hash) through different tool chains — a local GUI cracker (JTR/Johnny) versus two browser-based Networkwalks tools. Either approach reaches the same result quickly because the target passwords are short and dictionary-guessable, demonstrating how fast weak passwords fail against publicly available tools.
Part of the Networkwalks Cybersecurity Internship — Batch B084.
Lab files and target PDFs provided by Networkwalks for training purposes only.
