# Octopus an open source command and control C2 framework

Octopus is an open source, pre-operation C2 server.  It is based in Python and typically uses a powershell agent on the target server which it communicates with on HTTPS.  



![Screenshot (4)](https://github.com/Hacosta21/Threat-Hunting-with-Zeek-and-RITA/assets/65152491/6fb36c6c-1199-43bf-a7b3-91c8ae5d7946)
Octopus 24hr pcap sample.  

![Screenshot (5)](https://github.com/Hacosta21/Threat-Hunting-with-Zeek-and-RITA/assets/65152491/3038f067-08b6-4804-a1c8-e89f47773184)
Applied Zeek tool to process pcap file and parse file into Zeek log data. (conn.log, ssl.log, packet_filter.log, x509.log)


![Screenshot (25)](https://github.com/Hacosta21/Threat-Hunting-with-Zeek-and-RITA/assets/65152491/5358af9a-c96d-400e-8f9c-2ea3b4170d82)
Searching for connection persistency.  Looking at originating IP, responding IP as well as the duration of each connection.

![Screenshot (23)](https://github.com/Hacosta21/Threat-Hunting-with-Zeek-and-RITA/assets/65152491/851a1da5-5d64-4ddf-89a7-cd8dc11f4078)
The Pcap sample exhibits persistency on TCP port 443 and is using SSL Service. It also shows that the byte size of the connection traffic is relatively small compared to normal network traffic operating on the same port and service.



Real Intelligence Threa Analytics(RITA) tool, is open source and is designed to identify malicious activity within network traffic.
![Screenshot (31)](https://github.com/Hacosta21/Threat-Hunting-with-Zeek-and-RITA/assets/65152491/b7a7b0eb-cec8-45a0-ad4b-bc759ba5b296)
Analyzing the pcap sample with RITA produces a perfect beaconing score . Rita provides confirmation that this connection is beaconing and is worth further investigation.  


![Screenshot (15)](https://github.com/Hacosta21/Threat-Hunting-with-Zeek-and-RITA/assets/65152491/6cbba332-9447-412b-90bc-cef7dc749b67)




