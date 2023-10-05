# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
## PROGRAM:
Find out the ip address of the attackers system
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/0d04dd65-9cac-40e4-9e40-64d80555eb8c)
## invoke msfconsole:
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/796d67e1-eb34-4c95-9443-68ae5813845f)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

## OUTPUT:
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/77679638-81eb-4074-ac6c-467e5ad56813)
Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

## OUTPUT:
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/c85cb26f-fb0f-4c9d-8469-97482e0d5be6)
Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

## OUTPUT:
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/d6f6a588-d362-443e-add5-660fe8bcbc18)
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/152c1230-0d6b-44b9-821e-a035dd88ff31)
Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit.
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/23900dff-8cfa-4be4-9928-aea0b009f0b3)
The info command provides information regarding a module or platform.

## OUTPUT:
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/33c9ee57-b782-4543-b04f-18bfb14a2471)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>.
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/f4814f3d-f3b8-47d2-8568-bc350e6614b8)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql.
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/d740077c-4255-4115-a549-12c300fadbcd)
Use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version.
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/bac48ac4-249a-4a69-b436-cd412536fab1)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/9f99731b-91c0-4bca-9f59-5eacaf7c0b4f)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true.
![image](https://github.com/Udhayasankaran04/Metasploit-for-reconnaissance/assets/119393933/a5f61976-26c9-4d54-88fe-6fb0d24938be)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
