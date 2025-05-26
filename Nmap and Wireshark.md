This is a Walkthrough to set up and use The NMAP and Wireshark.
In this walkthrough we are using a TryHackMe vulnerable machine.
Note: Do not Scan any IP or URL without permission. It is ILLEGAL to perform scanning on any IP/URL without permission.
1.First lets install our tools.
    •Nmap:-
	    -To download Nmap lets go to its official Github page:- https://github.com/nmap/nmap
	-Click on the Code (Green button) and copy the url.
	 ![Image](https://github.com/user-attachments/assets/ec79b330-2041-4563-b65d-1768edde91c4)
        
-Type the Code in your terminal:- git clone url-you-copied
	    -Your nmap is successfully installed.
	    -You can access by typing “nmap” in your terminal.
     ![Image](https://github.com/user-attachments/assets/bfdc98e0-de0b-4f79-9a72-c83df468f23e)

	
•Wireshark:-
   -To download Wireshark lets go to its official Github page:- https://github.com/wireshark/wireshark
       ![Image](https://github.com/user-attachments/assets/ac5a655c-d836-43dd-98d0-24930826a988)
 
  -Follow the same procedure clone it using the url in your terminal.
        ![Image](https://github.com/user-attachments/assets/10545aa4-528b-497e-87b4-70614ed1af79)


2.	Now that we have installed Nmap and Wireshark lets do some basic scans and capture the packets. 
     ![Image](https://github.com/user-attachments/assets/6a99f95a-ee76-4af2-b421-b00e695c8f60)

3.	We can see the basic syntax for nmap:- nmap ip.
    •	The Scan shows the open ports which are:- 22 and  80.

4.	Let’s do some advanced attacks.
   ![Image](https://github.com/user-attachments/assets/97834b8a-8955-4a1e-8fd5-cd03d6bfc36e)

    •In this scan we have used some flags like –d –v –sV and –p-.
    •-d is for debugging.
    •-v is for verbosity.
    •-sV is to scan for the version.
    •-p is used to specify the ports to scan.
    •We can also use –oN <filename> flag for saving the the scan result.

5.	Security Risks
    •Port 80  can be used to access the webpage using http protocol. Which is not a secure protocol because it communicate in plain text.
    •We also has 22 SSH port open which is used to connect to any device remotely. SSH is a secure protocol but if someone knows any username and password they can use it to take reverse shell using it.

6.	Lets open Wireshark in the backgroud for packet sniffing and run the Nmap scan .
 	 ![Image](https://github.com/user-attachments/assets/f4373098-65cf-41c5-89e5-6fd0f65aba34)

7.	You can also use filters to filter out the packets.
    •We have used tcp.port==80 udp.port=80. Using this filter we can filter out all the tcp and packets transferred using port 80.
 	 ![Image](https://github.com/user-attachments/assets/b6e3ff02-fa07-42b1-b89b-6e2080c33887)
