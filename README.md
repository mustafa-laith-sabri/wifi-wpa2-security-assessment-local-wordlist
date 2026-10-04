# 🛡 Wireless Security Assessment: WPA2 Custom Dictionary Attack (Zain Iraq Format)

📌 Project Overview/ 
This project demonstrates a practical security assessment of a home WPA2 Wi-Fi network using a targeted dictionary attack. Instead of relying on generic
wordlists, a custom dictionary was generated based on local phone number patterns (Zain Iraq format: 11 digits starting with 078) to simulate a realistic localized
penetration testing scenario.

⚙️ Execution Phases & Methodology /
Phase 1: Custom Wordlist Generation (crunch)
Generating an exhaustive wordlist targeting Zain Iraq mobile numbers (11 digits starting with 078).
![Crunch Phase 3](https://github.com/mustafa-laith-sabri/wifi-wpa2-security-assessment-local-wordlist/blob/main/images/crunch%20%201.png)

![Crunch Phase 2](images/crunch%202.png)

![Crunch Phase 3](https://github.com/mustafa-laith-sabri/wifi-wpa2-security-assessment-local-wordlist/blob/main/images/crunch%20%203.png)

![Crunch Phase 4](images/crunch%204.png)


Phase 2: Adapter Preparation & Monitor Mode Activation
Configuring the wireless network adapter (wlan0) to enable Monitor Mode, allowing full packet capture across surrounding wireless channels.


![WLAN Phase 1](images/wlan%201.png)


Phase 3: Capturing the WPA2 4-Way Handshake
Monitoring target AP traffic and capturing the EAPOL 4-Way Handshake during client re-authentication.

![WLAN Phase 2](images/wlan%202.png)

![WLAN Phase 3](images/wlan%203.png)

![WLAN Phase 4](images/wlan%204.png)

![WLAN Phase 5](images/wlan%205.png)

![WLAN Phase 6](images/wlan%206.png)

![WLAN Phase 7](images/wlan%207.png)


Phase 4: Offline Cracking using aircrack-ng
Performing an offline dictionary attack by matching the captured handshake file against the customized Zain Iraq wordlist to recover the network key.

![Crack Phase 1](images/crack%201.png)

![Crack Phase 2](images/crack%202.png)

🔒 Security Recommendations...
Avoid Predictable Passphrases: Never use mobile phone numbers, national IDs, or sequential numbers as Wi-Fi passwords.

Use Strong Passphrases: Combine uppercase, lowercase, numbers, and special symbols with at least 12+ characters.

Upgrade to WPA3: Transition to WPA3-Personal which uses SAE (Simultaneous Authentication of Equals) to mitigate offline dictionary attacks.


👤 Author /
Name: Mustafa Layth Sabri
Certifications: CompTIA A+ | IBM IT Support Professional | CEH (In Progress)
