README.md

Included: DHCPserver.c, DHCPclient.c

Compilation: 

gcc -o DHCPserver DHCPserver.c

gcc -o DHCPclient DHCPclient.c

Execution:

On CSE01 give the command

./DHCPserver <portnumber>

Likewise on CSE02 - CSE06

./DHCPclient <portnumber>

Details & Explanation:

The program is a client-server program that is able to serve clients simutaneously by using the select() call on one socket. This client-server program is a simulation of a DHCP 4-way handshake, which shows the transactions of messages between client and server when assigning the necessary fields to the client and server for a given IP address. The file for available addresses is opened and given to the client, then put at the end of the file for updating later on. If the clients use up all 10 IP addresses then the program simply exits. In the code there is a time variable that gives an example of how it would be implmented by showing an elapsed time and using sleep of 5 seconds to show the elapsed time. If this were a requirement, an if statement would be wrote to check if(elapsed time was greater than 3600) - then free that IP address that client is using for another client to use. NOTE to the grader - You can comment out the sleep statement to show program working for multiple clients. If send requests to the server before the sleep is done the program starts behaving weird.
