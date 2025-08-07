Checking for Open Ports Using Nmap 

Step 1: Download and install the most compatible version of the Nmap on the Nmap official website. 
Step 2: Change to the directory you installed Nmap into. You can skip this step if Nmap is already in your command path (the installer adds it there by default). Otherwise, type the following commands.
c:
cd "\Program Files (x86)\Nmap"


Step 3: To perform a basic scan of the 1000 most commonly used ports on a target, use the following command, replacing <target> with the IP address or hostname of the system you want to scan. In this case, the local system IP address is 102.88.112.141. Therefore the following command apply.
Nmap –Pn 102.88.112.141


Step 4: scan a specific port.
To scan a single, specific port, use the –p or -Pn option followed by the port number
E.g 

nmap -Pn 80 102.88.112.141

NOTE: 
	The "-F" parameter sets the scan to only test the top 100 popular ports.
 
	The "-sS" parameter sets the scan type to SYN scan. The SYN scan is the most reliable scan option as it simulates the initial communication attempt from a valid client, while not completing the establishment of a full session. Therefore, the SYN scan has the best chance of determining the open state of TCP ports.
 
	The "-O" parameter attempts to identify the operating system.
 
	The "-Pn" parameter disables host discovery and assumes all IPs are actively in use.
	The "-oN" parameter saves the output of nmap to the specified filename (in addition to the screen display of the same).

