---
layout: post
title: "TryHackMe: RootMe Walkthrough"
date: 2025-05-15 10:00:00 +0530
categories: Capture the Flag, Walkthrough
---

![Room Banner](/assets/images/root-me/banner.png)

## 🛡️ Room: Room Name

**Difficulty:** Easy 
**Platform:** TryHackMe  
**Tags:** Enumeration, Exploitation, PrivEsc

---

## 🔍 Reconnaisance

Firstly, we will do nmap scan of the machine to see the open ports.

![Nmap Scan](/assets/images/root-me/nmap-scan.png)

So in this machine, we can see there are 2 ports open
1. Port 22 - SSH
2. Port 80 - HTTP

Now, We can find directories in the web server using Gobuster

![Gobuster results](/assets/images/root-me/Gobuster-result.png)
Here we can see, we found a directory /panel/, lets look into it now
![Website](/assets/images/root-me/website-view.png)

## Exploitation

As we can see we have an option to upload a file in it.
now, lets try to upload reverse shell payload to see if it works or not
![payload](/assets/images/root-me/payload.png)

We made a php reverse shell payload and saved it as shell.php

Now let's see what happens if we upload it, but before we need to start listener

![listener](/assets/images/root-me/listener.png)

We have started metasploit listener for reverse shell

Let's upload the file

![output](/assets/images/root-me/output1.png)

It showed error when we upload the shell.php file

After that, i tried php alternative php2,php3 and php5

as we see php5 worked out and we got the shell
![output](/assets/images/root-me/success-output.png)

![shell](/assets/images/root-me/shell.png)

As we can see we got the reverse shell 

![Flag](/assets/images/root-me/user-flag.png)

We got the flag using find command, as seen in the above image

## Privilege Escalation

Now let's see how to escalate privilege

From the question asked, we can see that we need to find a file with SUID permission
let's use "find" again to find the file

![Finding file for PrivEsc](/assets/images/root-me/SUID-file.png)

we can see there is python which has SUID bit, means if we can get root privilege if we execute it

![Privilege Escalation](/assets/images/root-me/privesc.png)

Here, used thes python command to set the UID to 0(root) and spawns a shell, as it has SUID bit, it will spawn the root shell

Here is the root flag
![Root Flag](/assets/images/root-me/flag.png)
