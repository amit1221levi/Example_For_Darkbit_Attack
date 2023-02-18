# Example_For_Darkbit_Attack
DarkBit, an unknown group, launched a devastating ransomware attack on my university, Technion - Israel Institute of Technology. The attack had a profound impact.
. As a computer science student, I was naturally intrigued by the attack much more than the exams and decided to investigate. 
let's go through the details of the DarkBit attack, including the attack  various components, and practical tips to prevent similar attacks

The DarkBit ransomware attack is a type of malicious software that is designed to target Windows operating systems. Once the malware is executed, it creates a Global mutex to ensure that only one instance of the malware is running at a time and then identifies all mounted drives on the victim's machine using the GetLogicalDrives() API and determines the drive type of each drive using the GetDriveType() API.

After identifying the files on the drives, the ransomware uses hardcoded configuration files in the ransomware binary to exclude certain file extensions, file names, and directory names from the encryption process. The ransomware then divides larger files into smaller segments as per the size limit given in the configuration file and encrypts each of these smaller segments individually.

The ransomware employs multithreading for its encryption process, using several APIs such as NtDeviceIoControlFile(), GetQueuedCompletionStatusEx(), PostQueuedCompletionStatus(), and ResumeThread(). The ransomware uses two worker threads to encrypt files on the victim’s machine.

After eliminating the list of files and folders, the ransomware proceeds to encrypt files on the victim's machine, appending the “.Darkbit” extension to the encrypted files. It also drops a ransom note named “RECOVERY_DARKBIT.txt” and includes a marker “DARKBIT_ENCRYPTED_FILES” and encryption details, such as the encryption key, at the end of the encrypted file.

To prevent ransomware attacks like the DarkBit :

Limit user privileges to avoid ransomware from spreading to critical systems and data

Implement access controls and use security solutions like firewalls, intrusion detection systems, and anti-virus software

Regularly backup critical data and store it offline or in a secure separate location

Keep all software up-to-date with the latest security patches and updates

Educate employees on how to identify and avoid phishing emails and social engineering tactics used by cybercriminals

Provide training on how to report suspicious emails and attachments        to IT staff

Conduct regular vulnerability assessments and penetration testing

DarkBit ransomware attack, better be the last cyber attack for a while, at least until I will bit you all with some Quantum Technology ;)

Thanks for reading and remember safe computer system is a happy computer system, 
 for the students, stay awesome and keep learning! 
