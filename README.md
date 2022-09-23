# boot2root

#### Result nmap scanning
```
➜  ~ nmap -sP 192.168.42.1-254
Starting Nmap 7.80 ( https://nmap.org ) at 2022-09-23 17:03 CEST
Nmap scan report for laptop (192.168.42.1)
Host is up (0.000069s latency).
Nmap scan report for 192.168.42.3
Host is up (0.00035s latency).
Nmap done: 254 IP addresses (2 hosts up) scanned in 5.76 seconds
➜  ~ nmap  192.168.42.3     
Starting Nmap 7.80 ( https://nmap.org ) at 2022-09-23 17:04 CEST
Nmap scan report for 192.168.42.3
Host is up (0.00014s latency).
Not shown: 994 closed ports
PORT    STATE SERVICE
21/tcp  open  ftp
22/tcp  open  ssh
80/tcp  open  http
143/tcp open  imap
443/tcp open  https
993/tcp open  imaps
```
### to  check 

- [ ] service de messagerie (protocol imaps)
- [ ] http://192.168.42.3/
	```
	➜  ~ curl -v http://192.168.42.3:80
	*   Trying 192.168.42.3:80...
	* Connected to 192.168.42.3 (192.168.42.3) port 80 (#0)
	> GET / HTTP/1.1
	> Host: 192.168.42.3
	> User-Agent: curl/7.81.0
	> Accept: */*
	> 
	* Mark bundle as not supporting multiuse
	< HTTP/1.1 200 OK
	< Date: Fri, 23 Sep 2022 15:12:58 GMT
	< Server: Apache/2.2.22 (Ubuntu)
	< Last-Modified: Wed, 07 Oct 2015 23:37:54 GMT
	< ETag: "3552-401-5218c3c475880"
	< Accept-Ranges: bytes
	< Content-Length: 1025
	< Vary: Accept-Encoding
	< Content-Type: text/html
	< X-Pad: avoid browser bug
	< 
```

- [ ] https://192.168.42.3/ (apache/2.2.22)
