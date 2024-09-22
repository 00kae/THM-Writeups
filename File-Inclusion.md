/r/room/fileinc

# File Inclusion
This room focuses on file inclusion vulnerabilities such as Local File Inclusion, Remote File Inclusion, and directory traversal. Wikipedia says its a vulnerability found in web application run times. 
One of the issues is input validation, meaning that users have unwarranted access
to inputs. If it is not validated, users can exploit this and access unintended items, such as data and credentials. The attacker can also write these files and gain remote command execution.


# Path/Directory Traversal
Path/Directory Traversal is a web security vulnerability that allows an attacker to read OS resources. By using the web application's URL, if it is not verified, can be easily accessed if not directly in the root directory of the application. 

These attacks takes advantage of moving through directories to get to an intended goal/file. If the door of a house is not locked and the lights are off, if the entry point/door is open, then the attacker can check each door and find whatever valuables he intended to steal.

Specifically with PHP, there is a function called `file_get_contents` that will read an entire file into one string. This function, paired with poor input validation, results in this vulnerability.

# Dot-dot-slash Attack
By using `../`, an attacker can traverse through a web application's directories, so long as they have an access point, which for example could be `get.php?file=`. 

Different servers, not surprisingly, require different paths in order to traverse.

# Lab 1: Local File Inclusion
It's important to note that these labs use PHP, but other languages such as ASP, JSP, or Node.js also can be exploited with LFI. 
We apply the knowledge written from the lecture to find `/etc/passwd`.

