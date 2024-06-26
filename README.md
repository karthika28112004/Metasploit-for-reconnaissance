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
```
NAME : KARTHIKA E
REGISTER NUMBER : 212222040072
```

## EXECUTION STEPS AND ITS OUTPUT:
Find out the ip address of the attackers system
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/9cce23b8-75df-4dbb-91ee-d92a1cde451b)

Invoke msfconsole
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/3c4c4112-ca9b-4781-9275-e103139a35f3)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/49182654-3bc4-4380-9020-a42b34567002)

Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/917942dd-ae7d-4d3a-942c-ade70a11cad6)

use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later. scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24 
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/e82154ef-6d0d-451b-819b-b30dd596a8b8)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/e566562d-24b3-4d26-8f3a-a14c7fd14d49)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/b47b34e4-95bc-4cc5-a0b3-0f9c6663febc)

The info command provides information regarding a module or platform
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/d697e333-86ae-4527-9015-2fa87db2e2f5)

Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/f65036b0-446a-4bfe-ae88-b6705a567a5e)

Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/be40d83d-63ad-4435-be5e-eec1a9751a1f)

use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/101046c1-8ab9-48dd-ab35-342d28f786e6)

Use the set rhosts command to set the parameter and run the module, as follows:
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/1ef3d37f-38bb-4e85-a121-4804e9d9b4f8)

After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module. 
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/34e9939f-7b7c-4f85-b597-7d9698c2505f)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true
![image](https://github.com/karthika28112004/Metasploit-for-reconnaissance/assets/128035087/a8f3489f-6728-432b-8d9b-8f5ccce00250)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully.
