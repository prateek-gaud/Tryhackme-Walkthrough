# Steel Mountain

<img width="447" height="740" alt="image" src="https://github.com/user-attachments/assets/9dfc49b2-6e0f-4771-bd20-550c9aa8a287" />


## Scanning:-
starting with the nmap scan.
```
$ nmap -Pn 10.49.152.245 -A -vv
Starting Nmap 7.99 ( https://nmap.org ) at 2026-08-19 02:27 +0530
NSE: Loaded 158 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:27
Completed NSE at 02:27, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:27
Completed NSE at 02:27, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:27
Completed NSE at 02:27, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 02:27
Completed Parallel DNS resolution of 1 host. at 02:27, 0.50s elapsed
Initiating SYN Stealth Scan at 02:27
Scanning 10.49.152.245 [1000 ports]
Discovered open port 139/tcp on 10.49.152.245
Discovered open port 8080/tcp on 10.49.152.245
Discovered open port 135/tcp on 10.49.152.245
Discovered open port 3389/tcp on 10.49.152.245
Discovered open port 445/tcp on 10.49.152.245
Discovered open port 80/tcp on 10.49.152.245
Discovered open port 49154/tcp on 10.49.152.245
Discovered open port 5985/tcp on 10.49.152.245
Discovered open port 49152/tcp on 10.49.152.245
Discovered open port 49156/tcp on 10.49.152.245
Discovered open port 49155/tcp on 10.49.152.245
Discovered open port 49153/tcp on 10.49.152.245
Completed SYN Stealth Scan at 02:27, 2.09s elapsed (1000 total ports)
Initiating Service scan at 02:27
Scanning 12 services on 10.49.152.245
Stats: 0:00:29 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 58.33% done; ETC: 02:28 (0:00:19 remaining)                                                                                                                                                                      
Stats: 0:00:35 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan                                                                                                                                                                 
Service scan Timing: About 58.33% done; ETC: 02:28 (0:00:23 remaining)                                                                                                                                                                      
Completed Service scan at 02:28, 60.82s elapsed (12 services on 1 host)                                                                                                                                                                     
Initiating OS detection (try #1) against 10.49.152.245                                                                                                                                                                                      
Initiating Traceroute at 02:28                                                                                                                                                                                                              
Completed Traceroute at 02:28, 3.01s elapsed                                                                                                                                                                                                
Initiating Parallel DNS resolution of 2 hosts. at 02:28                                                                                                                                                                                     
Completed Parallel DNS resolution of 2 hosts. at 02:28, 0.50s elapsed                                                                                                                                                                       
NSE: Script scanning 10.49.152.245.                                                                                                                                                                                                         
NSE: Starting runlevel 1 (of 3) scan.                                                                                                                                                                                                       
Initiating NSE at 02:28                                                                                                                                                                                                                     
Completed NSE at 02:28, 5.95s elapsed                                                                                                                                                                                                       
NSE: Starting runlevel 2 (of 3) scan.                                                                                                                                                                                                       
Initiating NSE at 02:28                                                                                                                                                                                                                     
Completed NSE at 02:28, 0.46s elapsed                                                                                                                                                                                                       
NSE: Starting runlevel 3 (of 3) scan.                                                                                                                                                                                                       
Initiating NSE at 02:28                                                                                                                                                                                                                     
Completed NSE at 02:28, 0.00s elapsed                                                                                                                                                                                                       
Nmap scan report for 10.49.152.245                                                                                                                                                                                                          
Host is up, received user-set (0.070s latency).                                                                                                                                                                                             
Scanned at 2026-08-19 02:27:42 IST for 74s                                                                                                                                                                                                  
Not shown: 988 closed tcp ports (reset)                                                                                                                                                                                                     
PORT      STATE SERVICE       REASON          VERSION
80/tcp    open  http          syn-ack ttl 126 Microsoft IIS httpd 8.5
|_http-server-header: Microsoft-IIS/8.5
|_http-title: Site doesn't have a title (text/html).
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
135/tcp   open  msrpc         syn-ack ttl 126 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 126 Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds  syn-ack ttl 126 Microsoft Windows Server 2008 R2 - 2012 microsoft-ds
3389/tcp  open  ms-wbt-server syn-ack ttl 126 Microsoft Terminal Services
| ssl-cert: Subject: commonName=steelmountain
| Issuer: commonName=steelmountain
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2026-08-17T20:54:56
| Not valid after:  2027-02-16T20:54:56
| MD5:     5caf c5d7 8283 7fb2 4252 83cf ad9b 38f4
| SHA-1:   1b6f 6fab 3285 0619 16f1 7925 fc3b 154f a7f5 f039
| SHA-256: 2ad0 b238 f4d4 27ed 8439 8a45 2782 3a32 f58f dda7 47ff 9fd6 56bc 192c 8d6d b3b0
| -----BEGIN CERTIFICATE-----
| MIIC3jCCAcagAwIBAgIQHYHyIXhxD7RBpBeb7V1N0TANBgkqhkiG9w0BAQUFADAY
| MRYwFAYDVQQDEw1zdGVlbG1vdW50YWluMB4XDTI2MDgxNzIwNTQ1NloXDTI3MDIx
| NjIwNTQ1NlowGDEWMBQGA1UEAxMNc3RlZWxtb3VudGFpbjCCASIwDQYJKoZIhvcN
| AQEBBQADggEPADCCAQoCggEBAN0sQE2mgzH1/p6RY95JjBdlIIAUpp0ZoEhvB6gc
| PgLOJS4aHl3z2w8KraQ+piHHa5lCeFVkRDcjmEK46mtJ8rrWIgE6cqLfmqnRm3KV
| IrNrwWK7LG1EnVwXV2muHaqBqNW1v6x18gETNcA6bb7UD1rzt3i+XgsVTT/Aw82u
| MZTMxVHFt/CDBhs5vWEcgvM/T6Is5wjQ0D/v/3/dd50C0FJ9qj5WrwVL0eh71iYh
| +KIn1MM3ueC5K0wunZRgfbWiHGoJ/OFTCUXVwbpp2AHMyAnhgJsE4Qt1mAZQ0xGy
| JyvKtKI/pt1GQCpx8QLYB3T9P1i/EGX9PkeXBpdMwxZ0I50CAwEAAaMkMCIwEwYD
| VR0lBAwwCgYIKwYBBQUHAwEwCwYDVR0PBAQDAgQwMA0GCSqGSIb3DQEBBQUAA4IB
| AQCdnJhEbOv0vI/bYTO0h7WiwlOTfnlTYOyHjj+FBDxvU5Oj+IUN50/1O3ZKXRcs
| 0wAeUQEQNv8BCCoAS7g2KWAq1JNmHHz68Srh1RxghfK40o7ChuYFsbeMh3qwvgVt
| /zpozwcq6hNRv2AA3MFtMPQOKnAYY+eSt1aHjLWdi1It9R+3zVCaPoaLckF4CRFb
| Dm7UfT7XJhk6yjZs32q5DfOb4UHU/x0NoELCli7oV5uqR0IxrejsPk2hRoHTAj9R
| NJ2DqRLUE4N61SzG2tHY1RNvmdgETQ0H+ra3OqHHM5ESmx6+QZ375PZQYmr57rJQ
| hGlU+gKDsUlhJ2uTGfVgZH2R
|_-----END CERTIFICATE-----
| rdp-ntlm-info: 
|   Target_Name: STEELMOUNTAIN
|   NetBIOS_Domain_Name: STEELMOUNTAIN
|   NetBIOS_Computer_Name: STEELMOUNTAIN
|   DNS_Domain_Name: steelmountain
|   DNS_Computer_Name: steelmountain
|   Product_Version: 6.3.9600
|_  System_Time: 2026-08-18T20:58:50+00:00
|_ssl-date: 2026-08-18T20:58:56+00:00; 0s from scanner time.
5985/tcp  open  http          syn-ack ttl 126 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
8080/tcp  open  http          syn-ack ttl 126 HttpFileServer httpd 2.3
|_http-title: HFS /
| http-methods: 
|_  Supported Methods: GET HEAD POST
|_http-favicon: Unknown favicon MD5: 759792EDD4EF8E6BC2D1877D27153CB1
|_http-server-header: HFS 2.3
49152/tcp open  msrpc         syn-ack ttl 126 Microsoft Windows RPC
49153/tcp open  msrpc         syn-ack ttl 126 Microsoft Windows RPC
49154/tcp open  msrpc         syn-ack ttl 126 Microsoft Windows RPC
49155/tcp open  msrpc         syn-ack ttl 126 Microsoft Windows RPC
49156/tcp open  msrpc         syn-ack ttl 126 Microsoft Windows RPC
Device type: general purpose
Running: Microsoft Windows 2012
OS CPE: cpe:/o:microsoft:windows_server_2012:r2
OS details: Microsoft Windows Server 2012 or 2012 R2
TCP/IP fingerprint:
OS:SCAN(V=7.99%E=4%D=8/19%OT=80%CT=1%CU=41208%PV=Y%DS=3%DC=T%G=Y%TM=6A84C79
OS:0%P=x86_64-pc-linux-gnu)SEQ(SP=FC%GCD=1%ISR=10C%TI=I%CI=I%II=I%SS=S%TS=7
OS:)OPS(O1=M4E8NW8ST11%O2=M4E8NW8ST11%O3=M4E8NW8NNT11%O4=M4E8NW8ST11%O5=M4E
OS:8NW8ST11%O6=M4E8ST11)WIN(W1=2000%W2=2000%W3=2000%W4=2000%W5=2000%W6=2000
OS:)ECN(R=Y%DF=Y%T=80%W=2000%O=M4E8NW8NNS%CC=Y%Q=)T1(R=Y%DF=Y%T=80%S=O%A=S+
OS:%F=AS%RD=0%Q=)T2(R=Y%DF=Y%T=80%W=0%S=Z%A=S%F=AR%O=%RD=0%Q=)T3(R=Y%DF=Y%T
OS:=80%W=0%S=Z%A=O%F=AR%O=%RD=0%Q=)T4(R=Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD=0
OS:%Q=)T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=80%W=0%S
OS:=A%A=O%F=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R
OS:=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N
OS:%T=80%CD=Z)

Uptime guess: 0.005 days (since Wed Aug 19 02:22:22 2026)
Network Distance: 3 hops
TCP Sequence Prediction: Difficulty=252 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: OSs: Windows, Windows Server 2008 R2 - 2012; CPE: cpe:/o:microsoft:windows

Host script results:
| nbstat: NetBIOS name: STEELMOUNTAIN, NetBIOS user: <unknown>, NetBIOS MAC: 0a:44:1f:8e:f5:09 (unknown)
| Names:
|   STEELMOUNTAIN<00>    Flags: <unique><active>
|   WORKGROUP<00>        Flags: <group><active>
|   STEELMOUNTAIN<20>    Flags: <unique><active>
| Statistics:
|   0a 44 1f 8e f5 09 00 00 00 00 00 00 00 00 00 00 00
|   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
|_  00 00 00 00 00 00 00 00 00 00 00 00 00 00
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 51249/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 34487/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 28667/udp): CLEAN (Timeout)
|   Check 4 (port 16693/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb-security-mode: 
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb2-security-mode: 
|   3.0.2: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2026-08-18T20:58:50
|_  start_date: 2026-08-18T20:53:28
|_clock-skew: mean: 0s, deviation: 0s, median: 0s

TRACEROUTE (using port 995/tcp)
HOP RTT       ADDRESS
1   144.22 ms 192.168.128.1
2   ...
3   144.51 ms 10.49.152.245

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:28
Completed NSE at 02:28, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:28
Completed NSE at 02:28, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:28
Completed NSE at 02:28, 0.00s elapsed
Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .


Nmap done: 1 IP address (1 host up) scanned in 74.81 seconds
           Raw packets sent: 1104 (49.290KB) | Rcvd: 1079 (43.954KB)
```

## Enumeration:-
Here I can see some important ports are open 
```
PORT      STATE SERVICE       REASON          VERSION
80/tcp    open  http          syn-ack ttl 126 Microsoft IIS httpd 8.5
|_http-server-header: Microsoft-IIS/8.5
|_http-title: Site doesn't have a title (text/html).
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
135/tcp   open  msrpc         syn-ack ttl 126 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 126 Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds  syn-ack ttl 126 Microsoft Windows Server 2008 R2 - 2012 microsoft-ds
3389/tcp  open  ms-wbt-server syn-ack ttl 126 Microsoft Terminal Services
5985/tcp  open  http          syn-ack ttl 126 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
8080/tcp  open  http          syn-ack ttl 126 HttpFileServer httpd 2.3
```
And I open the website and http://10.49.152.245/ and I found the Employee of the month
<img width="1913" height="1039" alt="employee_of_the_month" src="https://github.com/user-attachments/assets/a23cb55b-84e4-44be-876c-12f75eb06ce9" />


I can see that netbios is running on port number 139 let's try to connect using smbclient.
```
┌──(jonathan㉿Anonymous)-[~/Documents/CTF/Tryhackme/Steel_Mountain]
└─$ smbclient -L '//10.49.152.245////'                       
Password for [WORKGROUP\jonathan]:
session setup failed: NT_STATUS_ACCESS_DENIED

```
It is not working.

After reviewing the scan result I found that one suspicious service is running on port 8080 which is HTTPFileServer and the version of this service is HttpFileServer httpd 2.3.
So, I search for the exploit on google and found the CVE and exploit for the version.

## Foothold:-

Download the exploit and use it:-
<img width="1908" height="868" alt="exploit" src="https://github.com/user-attachments/assets/c478d2ff-05fc-48dc-9112-afff926bc074" />

We Got The Initial Access... <br>
Let find our first flag usually the flag is located in the user Directory or Desktop
```
PS C:\Users\bill\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup> cd ..
PS C:\Users\bill\AppData\Roaming\Microsoft\Windows\Start Menu\Programs> cd ..
cd ..
cd ../PS C:\Users\bill\AppData\Roaming\Microsoft\Windows\Start Menu> .PS C:\Users\bill\AppData\Roaming\Microsoft\Windows> .
PS C:\Users\bill\AppData\Roaming> cd ../..
PS C:\Users\bill> ls


    Directory: C:\Users\bill


Mode                LastWriteTime     Length Name                                                                      
----                -------------     ------ ----                                                                      
d----         9/26/2019  11:29 PM            .groovy                                                                   
d-r--         9/27/2019   4:07 AM            Contacts                                                                  
d-r--         9/27/2019   9:08 AM            Desktop                                                                   
d-r--         9/27/2019   4:07 AM            Documents                                                                 
d-r--         9/27/2019   4:07 AM            Downloads                                                                 
d-r--         9/27/2019   4:07 AM            Favorites                                                                 
d-r--         9/27/2019   4:07 AM            Links                                                                     
d-r--         9/27/2019   4:07 AM            Music                                                                     
d-r--         9/27/2019   4:07 AM            Pictures                                                                  
d-r--         9/27/2019   4:07 AM            Saved Games                                                               
d-r--         9/27/2019   4:07 AM            Searches                                                                  
d-r--         9/27/2019   4:07 AM            Videos                                                                    


PS C:\Users\bill> cd Desktop
PS C:\Users\bill\Desktop> ls


    Directory: C:\Users\bill\Desktop


Mode                LastWriteTime     Length Name                                                                      
----                -------------     ------ ----                                                                      
-a---         9/27/2019   5:42 AM         70 user.txt                                                                  


PS C:\Users\bill\Desktop> cat user.txt
b04763b6fcf51fcd7c13abc7db4fd365
PS C:\Users\bill\Desktop> whoami /priv
```
We Get Our First Flag...

#### Questions:-
Q. Who is the employee of the month?
answer: Bill Harper <br>
Q. Scan the machine with nmap. What is the other port running a web server on?
answer: 8080 <br>
Q. What is the CVE number to exploit this file server?
answer: 2014-6287 <br>
Q. Take a look at the other web server. What file server is running?
answer: Rejetto HTTP File Server <br>
Q. Use Metasploit to get an initial shell. What is the user flag?
answer: b04763b6fcf51fcd7c13abc7db4fd365 <br>

## Privilege Escalation:-
After getting initial access to the machine. I checked for the Privileges and Cached Credentials and nothing found.
<img width="819" height="266" alt="priv_creds" src="https://github.com/user-attachments/assets/a6cc649b-c1b5-499e-997b-89c8848a6f1f" />

 searching for the service which is created by the user and for that I can use the Unquoted Service Paths command which I get from Hacktricks:-
```
gwmi -class Win32_Service -Property Name, DisplayName, PathName, StartMode | Where {$_.StartMode -eq "Auto" -and $_.PathName -notlike "C:\Windows*" -and $_.PathName -notlike '"*'} | select PathName,DisplayName,Name
```
<img width="1900" height="211" alt="Unquoted_service_path" src="https://github.com/user-attachments/assets/a90f583c-8e09-48f3-9275-d6edb6b7b737" />

Navigate to the C:\Program Files (x86)\IObit Path to check that we have permission to create any file or not you can simply check by creating a file or using any binary for permission check.






