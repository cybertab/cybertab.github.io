---
title: Unpacking Ransomware -The Anatomy of a Malicious Attack
date: 2023-02-16 20:00:00 +0400
categories: [cybersecurity, Ransomware]
tags: [ransomeware, rasomwarecycle, ransomwaregenerate, securityevasion]
---

# Ransomware & Its Entry points

Ransomware is a type of malicious software that encrypts a victim's files. The attackers then demand a ransom from the victim to restore access to the files, usually paid in cryptocurrency. The attackers threaten to permanently block access to the encrypted files if the ransom is not paid. Ransomware attacks can cause significant disruption and financial loss to individuals and organizations. It is important to regularly backup important data and keep software up-to-date to reduce the risk of a ransomware attack.

![R1](/assets/images/2023-02-16-Ransomware-%26-Its-Entry-points/R1.png

<pre>

</pre>

**Possible entry points from where a ransomware can enter into an organization:**

1. **Phishing Emails:** Attackers may send emails with malicious attachments or links that, when clicked, download and install the ransomware on the recipient's device.
2. **Malicious Websites:** Visiting a malicious website that exploits vulnerabilities in the web browser or operating system can lead to a ransomware infection.
3. **Software Vulnerabilities:** Outdated software, such as operating systems and applications, can have vulnerabilities that can be exploited by attackers to install ransomware.
4. **Remote Desktop Protocol (RDP):** Unsecured RDP connections can be used by attackers to gain unauthorized access to a network and spread ransomware.
5. **Removable Media:** USB drives or other removable media can be infected with ransomware and spread to other devices when connected.
6. **Watering Hole Attacks:** Attackers may compromise a website that is frequently visited by potential victims, such as those of a specific industry or organization, and use it to spread ransomware.
6. **Social Engineering:** Attackers may trick individuals into downloading and installing ransomware by posing as a trustworthy entity or by claiming that the software is a required update.

<pre>

</pre>

## Ransomware family:

1. Phishing Emails: **Emotet, Ryuk, TrickBot**
2. Malicious Websites: **Egregor, REvil, Clop**
3. Software Vulnerabilities: **WannaCry, Petya/NotPetya, Bad Rabbit**
4. Remote Desktop Protocol (RDP): **SamSam, Sodinokibi, Ryuk**
5. Removable Media: **ExPetr (a.k.a Petya, NotPetya), LockerGoga, Ryuk**
Watering Hole Attacks: **Jaff, Dharma, Apocalypse**
6.Social Engineering: **TeslaCrypt, Locky, Cerbe**

<pre>

</pre>


# Architecture - Ransomware devlopment 

1. **Research:** The attacker must research the target environment and identify potential vulnerabilities to exploit. This may involve gathering information about the target's software and hardware configurations, as well as identifying potential entry points, such as email addresses or remote access protocols.
2. **Design:** Based on the research, the attacker must design the ransomware to meet their specific goals and constraints. This may involve deciding on the encryption method to use, the ransom amount to demand, and the means of communication with the victim.
3. **Coding:** The attacker writes the code for the ransomware, taking care to avoid detection by anti-virus software and other security measures. They may use readily available tools, such as crypters or packers, to evade detection.
4. **Testing:** The attacker tests the ransomware in a controlled environment to ensure it functions as intended and to identify and fix any bugs.
5. **Distribution:** The attacker distributes the ransomware to potential victims, typically via phishing emails, malicious websites, or other methods of social engineering.

## Ransomware Operation in windows O.S from 0 to 1

1. **Network Propagation:** The ransomware will attempt to spread to other systems within the network, using techniques such as brute-forcing remote desktop protocol (RDP) credentials, exploiting network shares, or exploiting lateral movement techniques.
2. **File Discovery:** The ransomware scans the file system to identify files to encrypt. It may target specific file types, such as documents, images, and archives, or it may encrypt all files.
3. **Encryption:** The ransomware encrypts the targeted files using a strong encryption algorithm, such as AES or RSA. The encrypted files are typically marked with a unique extension, such as .locked or .enc, to indicate that they have been encrypted.
4. **Ransom Note Creation:** The ransomware creates a ransom note, either in the form of a text file or a splash screen, that informs the victim of the encryption and demands payment for the release of the encrypted data.
5. **Persistence Mechanism:** The ransomware sets up a persistence mechanism, such as a registry entry or scheduled task, to ensure that it will run automatically each time the system is rebooted.
6. **Data Exfiltration:** Some variants of ransomware may also exfiltrate sensitive data, such as personal information or intellectual property, before or during the encryption process.

<pre>

</pre>

# Security Controls evasion- Techniques

1. **Code obfuscation:** Ransomware code is often obfuscated or encrypted to evade detection by security controls.

2. **Anti-analysis techniques:** Ransomware authors use various techniques to detect when their malware is running in a sandbox or being analyzed by security researchers, and modify the malware behavior accordingly.

3. **Exploiting software vulnerabilities:** Ransomware can exploit unpatched software vulnerabilities to gain unauthorized access to a system.

4. **Social engineering:** Ransomware authors use social engineering techniques to trick users into downloading and executing the malware.

5. **Fileless malware:** Ransomware can use fileless techniques to inject malicious code into legitimate system processes, making it harder for security controls to detect the malware.

6. **Polymorphic malware:** Ransomware can use polymorphic techniques to change its code structure and evade signature-based detection.

7. **Encryption:** Ransomware uses advanced encryption algorithms to encrypt files and prevent access to them, making it harder for security controls to detect or reverse the damage.

8. **Network evasion:** Ransomware can use various techniques to evade network security controls and communicate with its command-and-control (C&C) server, such as using non-standard ports or protocols.

<pre>

</pre>

# Signs - Ransomware is on move already.


1. **Unusual network traffic:** Increased network traffic or traffic to unexpected or unauthorized locations may indicate a ransomware attack. This can include increased traffic to known command and control servers or sudden spikes in outbound traffic.
2. **Suspicious processes:** The presence of suspicious or unknown processes, especially those executing in user mode, may indicate a ransomware attack. This can include processes that are attempting to encrypt files or that are communicating with external servers.
3. **Altered or encrypted files:** The presence of encrypted or altered files, especially those that cannot be opened or modified, may indicate a ransomware attack. This may also include changes to file extensions, filenames, or the presence of ransom notes.
4. **Disabled security software:** The disabling or failure of security software, including anti-virus software, firewalls, and intrusion detection systems, may indicate a ransomware attack.
5. **Application crashes:** Application crashes or system failures, especially those that cannot be explained or resolved, may indicate a ransomware attack.
6. **Increased resource usage:** Increased resource usage, including high CPU or memory utilization, may indicate a ransomware attack. This may also include system slowdowns, unresponsiveness, or crashes.
7. **Network resource disruption:** The disruption or failure of network resources, including servers, storage devices, or network switches, may indicate a ransomware attack.

<pre>

</pre>


# Must Have Security controls to secure your organization from ransomware.

+ **File Signature Detection:** Security controls should use file signature detection to identify known malicious files and prevent them from executing on the target machine. File signature detection uses hashes, or digital fingerprints, of known malicious files to detect and prevent their execution.
+ **Heuristics-Based Detection:** Security controls should also employ heuristics-based detection to identify unknown or new variants of malware. Heuristics-based detection uses behavioral analysis and machine learning algorithms to identify malicious activity and prevent it from executing.
+ **Network Traffic Analysis:** Security controls should perform deep packet inspection on network traffic to detect and prevent the spread of malware within a network. This includes identifying and blocking malicious IP addresses, domain names, and command-and-control (C&C) servers.
+ **Endpoint Protection:** Security controls should provide endpoint protection to prevent malware from executing on individual systems and to prevent the spread of malware within a network. This includes anti-virus software, firewalls, and intrusion detection systems.
+ **Whitelisting:** Security controls should use whitelisting to allow only known and trusted applications to execute on a target machine. Whitelisting blocks all other applications, including malware, from executing.
+ **Application Control:** Security controls should provide application control to monitor and prevent the execution of malicious scripts, macros, and other malicious files.
+ **Email Filtering:** Security controls should provide email filtering to prevent phishing emails and other malicious emails from reaching end-users. This includes filtering for malicious attachments, links, and domain names.
+ **Patch Management:** Security controls should provide patch management to ensure that all software is up-to-date and secure. This includes regular software updates, security patches, and hotfixes.
+ **Backups:** Security controls should include regular backups of critical data to ensure that data can be restored in the event of a ransomware attack.


Till then stay vigilant and don't fall into any Cyber Trap.

Don't forget to:

```bash
sudo apt update && sudo apt upgrade
```

Stay Updated.