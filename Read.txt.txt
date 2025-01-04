Project: Hacking an FTP Server and Extracting Hidden Information

In this project, I performed a series of penetration testing tasks, which involved hacking an FTP server, extracting hidden data, and using various tools to work with network services and files.

My Steps:
Network Scanning:

First, I used nmap to scan the target server and identify open ports. This helped me find the FTP service running on port 21.
Brute-forcing FTP Authentication:

I used hydra to perform a brute-force attack on the FTP server. By using the rockyou.txt password list, I successfully guessed the password for the chris user (crystal), allowing me to log in.
Extracting Files from the FTP Server:

Once logged in, I downloaded several files, including To_agentJ.txt and images like cutie.png and cute-alien.jpg.
During the analysis of the cutie.png image, I discovered hidden data.
Analyzing Hidden Data:

I used binwalk to analyze the cutie.png image. This revealed embedded ZIP data at specific byte offsets.
Inside the ZIP archive (8702.zip), I found a text file (To_agentR.txt) containing crucial information.
Cracking the ZIP Password:

To extract the contents of the ZIP archive, I used zip2john to extract the password hash, followed by john the ripper to crack the password (alien).
With the correct password, I successfully extracted the To_agentR.txt file, which contained further secret messages.
Working with Extracted Data:

The information in the files pointed to hidden messages from agents and important clues for further steps.
This project allowed me to apply various penetration testing techniques, such as exploiting FTP servers, analyzing image files for hidden data, and using decryption tools to uncover important information.