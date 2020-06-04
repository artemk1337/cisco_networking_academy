# cisco_networking_academy

## Lab №1
### Switch Configuration.

1. Connect the switch to a personal computer with a console cable
2. Connect using Putty to manage the switch
3. Examine the status of the switch. Master the show Cisco IOS commands.
4. Perform the basic configuration of the switch: name, password encryption and passwords for entering privileged mode, prohibition of unwanted DNS lookups, banner message, new VLAN99, IP address of SVI interface VLAN99, default gateway. Restrict access through the console port. Restrict access on vty lines.
- A device name is assigned to enter a unique identification for this device.
- Password encryption so that passwords are displayed in encrypted form
- Entering privileged mode is password protected
- Prohibition of unwanted DNS lookup - it is set so that a syntactically incorrectly entered command is not perceived by the device as a DNS name query and then a DNS server search for a name resolution (which leads to significant time delays). In the simulated situation of addressing by DNS name, it is recommended to use the combination Ctrl + Shift + 6 to terminate the process.
- A banner message is configured to inform the connecting user about the illegality of unauthorized access to the device
- In order to be able to connect to the device via telnet, the device must be assigned an IP address. An IP address is assigned to the switch through the SVI virtual network interface. By default, the switch has only one known VLAN. Therefore, assigning an address to its interface is not recommended for security reasons. It is recommended to create a VLAN with a different number, and set the address on its interface. The choice of VLAN 99 is random, so you are not required to use VLAN 99 always.
- Configuring the default IP gateway is necessary because if no default gateway is configured, the switch cannot be controlled from a remote network that has more than one router on its way. Although this exercise does not take into account the external IP gateway, imagine that you later connect the LAN to the router for external access.
- Connection to the device via the console cable must be closed with a password; otherwise, anyone with console access poses a potential threat.
- Likewise, connecting to the device via remote access via telnet needs to be closed with a password. Each remote connection forms a vty line - a virtual connection. Password locks all possible vty lines. If you do not configure vty passwords, access to the device via Telnet will not be provided.
5.Test settings
6. Connect to the switch via telnet
7. Examine device connections and CAM table.

## Lab №2
### Switch Port Security.

1. Connect the switches according to the diagram.

2. LR2 - Scheme.png

3. Perform the initial setup of the switch.

4. Configure the switches with IP addresses in the range specified by the instructor. The VLAN number is also determined by the teacher.

5. Connect computers to the switches. Configure IP addresses for computers.

6. Note: To connect more devices to the switch (than provided by equipment in the classroom), you can use your own equipment (laptop).

7. Test all connections.

8. Analyze the switch CAM table; determine how many addresses it contains: whose addresses are these?

9. Determine what information can be obtained through CDP (use the help to explore the possibilities of CDP).

10. Examine the port settings (shutdown, duplex, and speed) for the ports connecting the computer to the switch and for the ports connecting the switches. Define combinations of settings in which a device connection is not established. The test plan needs to be developed independently.

11. Configure port security: set access mode for the port; enable security settings; set the maximum number of connections - 1 address and set the static address binding. Violate the security mode; check the result. Restore port status. Disable static address (or continue working with another port). The test plan needs to be developed independently.

12. Similarly, test the address binding by “sticking”. Violate the security mode; check the result. Restore port status. The test plan needs to be developed independently.


## Lab №3
### Switches. Work with VLAN.

1. Check how many virtual networks are currently present on the switch.

1. Delete the vlan.dat file.

1. Reboot the switch. Attention: if during a reboot you are prompted to save the current configuration before rebooting the switch as part of this lab, DO NOT save, answer no and press Enter.

1. Check how many virtual networks are currently present on the switch.

1. Create vlan <Your List Number>. Include ports 7 through 10 in it. Remove this vlan. Check what Vlan ports 7 through 10 are in. 1. 1. Restore the configuration.

1. Connect the switches according to the diagram:

1. LR3 - Scheme.png

1. Get instructions from the teacher on virtual network numbers and the distribution of network nodes (computers) by vlan. Before setting up the switches, develop an IP addressing scheme for network devices and check with your teacher.

1. Perform the initial configuration of the switch (in particular, determining the IP address) based on the instructions received.

1. Configure the specified vlan and ports to allow hosts to communicate within each vlan.

1. Test created vlan: if there are not enough nodes in the laboratory, switch existing nodes to the tested switch ports. The result: the interaction of all PCs within the same VLAN.

1. Test the ability to manage each switch from a single node using telnet.

1. Configure SSH on the switches.

1. Test the ability to manage each switch from a single node using telnet.

1. Test the ability to manage each switch from one host through SSH.

1. Disable SSH server.

1. Test the ability to manage each switch from a single node using telnet.



## Lab №4
### Configure a router. Statistical Routing.

1. Design the addressing of the scheme in accordance with the range of IP addresses specified by the teacher. Check it with the teacher.

1. Assemble the circuit.

1. Perform the initial configuration of "your" router.

1. Configure the addresses of the router interfaces.

1. Check and examine the routing table.

1. Configure PC IP settings.

1. Test network device interaction (ping): determine device availability and inaccessibility.

1. Make entries of remote networks in the routing table of the router. Check and examine the routing table. Test the interaction of network devices (ping and tracert): determine the availability and inaccessibility of devices.

1. Create a virtual interface on the router; Get directions to the virtual interface. To test.

1. Make an error in the routing table of one (or two) routers in order to simulate a packet loss situation after TTL expiration. To test. Fix the error.

1. Insert a floating static route. Check routing table.

1. Disconnect the main route (by physical disconnection of the wire or software shutdown). Check routing table. Test the floating route. Contact the network routers at the virtual interface address for management (or monitoring).


## Lab №5
### VLAN: DTP and VTP support protocols, routing between VLANs.

1. Learn the DTP protocol:

1. Enable switches. Check the operation modes of the interfaces with the show interfaces switchport command; pay attention to the Administrative Mode (which mode the port works on the switch) and Operation Mode (shows in which mode the ports agreed on operation).

1. Connect the switches in pairs (not yet configured).

1. Check the operating modes of the ports connecting the switches.

1. Set the port connecting the switches of ONE switch to the trunk. Check the operating modes of the ports connecting the switches.

1. Check the system configuration (running config) to find information about changing port modes on both switches.

1. Cancel port transition to trunk mode. Check port operation modes.

1. Learn the VTP protocol:

1. View information (show vtp status) about the vtp protocol on the switches; pay attention to the roles of switches, domain name and revision number.

1. Leave one switch VTP server, make the second switch a client. Create a domain name on the server.

1. View information (show vtp status) about the vtp protocol on the switches; pay attention to the roles of switches, domain name and revision number.

1. Create a new VLAN on the server. Check if the audit has passed to the client.

1. Set the switch port of the vtp server to trunk mode. Check if the audit has passed.

1. Put vtp client in server mode. Create another VLAN. To test.

1. Delete VLAN. To test.

1. Create a VLAN on a vtp client. To test.

1. Restore the original system configuration.

1. Creating multiple VLANs:

1. Connect the switches and personal computers according to the diagram:

1. Check with the teacher for details of the scheme; Obtain from the teacher the number of VLANs, VLAN numbers, VLAN IP addresses; develop an addressing scheme; coordinate it with the teacher before setting up the equipment. In the absence of the required number of PCs, prepare the ports entered into the required VLANs on the switches, test the circuits by switching the PC between the switches.

1. Delete the vlan.dat file on the switch. Reboot the switch.

1. Configure the equipment according to the scheme: set IP addresses on personal computers, on switches and on the subinterfaces of routers. Create VLANs on switches, associate ports with VLANs, create trunk channels, configure to support a given VLAN list.

1. Test routing between VLANs: each device should be able to ping any other device in the circuit.

## Lab №6
### Dynamic routing.

1. Develop an IP addressing plan for the proposed scheme. A typical laboratory workflow is shown below; the current scheme may differ from the above. Network addresses to discuss with the teacher. It is preferable to use addresses of the range 172.16.0.0-172.31.0.0 with the mask 255.255.255.0 for dead-end networks, and for the connecting networks the addresses of the range 192.168.0.0-192.168.255.0 with the mask 255.255.255.0 (for understanding auto-summarization of routes).

1. Perform initial configuration of personal computers and routers (IP-addresses and vty access if necessary).

1. Configure part of the circuit to use the RIPv2 protocol.

1. Check routing tables (show ip route) with auto-summarize routes enabled by default, and with auto-summarize routes disabled.

1. Examine routing table entries (show ip route): how many routes are in the table? source of routes? metric of each route?

1. Check the status of the interface using the show ip protocols command: which routing protocol is enabled? How often are protocol updates sent? when did the latest updates come? which interfaces are passive? What protocol version messages are received and sent?

1. To study the transmission of service packs (debug ip rip): from which interfaces is the transmission of updates carried out? What interfaces receive updates?

1. Clear the routing table. Test the result: check the status of the table after 15 seconds; after 30 seconds.

1. Configure part of the circuit to use the OSPF protocol.

1. Check the identifier of the OSFP router (show ip protocols), and also pay attention to the questions: which routing protocol is enabled? when did the latest updates come?

1. Examine routing table entries (show ip route): how many routes are in the table? source of routes? metric of each route?

1. To study the transmission of update packages (debug ip ospf events): from which interfaces is the transmission of updates performed? What interfaces receive updates?

1. To study OSPF processes, it is recommended to change the router id and delete the process. Observe the stages of convergence.

1. To study the OSPF metric, it is recommended to change the bandwidth or cost of the channel, check the entries in the routing tables. Change the specified channel bandwidth, check entries in the routing tables.

1. Both the RIP2 and OSPF must be installed on the edge router. Check the routing tables of the border router and other routers. Test the connection of the RIP and OSPF parts of the circuit. Result? Cause?

1. Configure default-information originate: for OSPF, a default route is required.

1. Combine the "extreme" routers of the circuit (in the above circuit 14 and 17). Test routing tables. Disconnect the connection between routers (for example, between 12 and 15). Test routing tables.

## Lab №7
### Configure DHCP with EIGRP support.

1. Assemble the circuit.

1. Get the address space from the teacher; develop the IP addressing of the circuit, check the IP addressing with the teacher; configure router interfaces.

1. On all routers, raise EIGRP. Test the settings: view the routing table; ping network routers.

1. For hosts, set the automatic receipt of IP parameters.

1. On all routers connected to nodes (in the above diagram, routers with numbers 1,2,5,6), configure DHCP. Test the provision of IP parameters to the nodes: check the provided parameters on the nodes; Check the provided addresses and request-response statistics on the servers and ping the network nodes.

1. Delete DHCP settings on routers with numbers 1,2,5,6.

1. Configure DHCP pools for all networks containing nodes on the “central” routers of the scheme (in the given scheme, routers with numbers 3 and 4). On routers with numbers 1,2,5,6, configure relay of the host request to the DHCP server. Test the provision of IP parameters to the nodes: check the provided parameters on the nodes; Check the provided addresses and request-response statistics on the servers and ping the network nodes.

## Lab №8
### VLAN: ACLs and their use for configuring NAT (+ PAT).

1. Obtain from the teacher IP addresses for the implementation of the scheme and design the scheme. Check the scheme with the teacher. Assemble the circuit and make settings in accordance with the plan.

1. Set up a dynamic routing protocol. Test communication between end nodes of the network.

1. Configure passwords on enable mode and on vty line input to provide telnet remote control. Test telnet connectivity from each device.

1. By creating (ip access-list standard) an access list to restrict telnet access to routers, leaving access from only one node (use permit for this node). In the process of defining an access list, examine the parameters of the ip access-list standard command using a space and a question mark. Apply access list on vty line as incoming.

1. Test telnet calls to routers from various nodes. Check statistics on access lists (show ip access-lists).

1. Change the created access list to add a deny any to it. Test telnet calls to routers from various nodes. Check statistics on access lists (show ip access-lists).

1. Set up a ban on accessing nodes of “extreme” networks (connected through switches 0 and 1) to the addresses of routers of only the “middle” (between 1 and 2 routers) networks, while maintaining access to all other addresses: use advanced access lists for configuration.

1. Configure dynamic NAT: according to the scenario of this part of the laboratory work, the Internet provider (Router 2) allocated to each company (networks with switches 0 and 1) ranges of 2 public IP addresses (for example, 12.12.12.0/30 and 12.12.12.4/30) . Thanks to this, each company received two public IP addresses.

1. To simulate Internet access, create an “external address” on R2 as a loopback interface (for example, 100.100.100.100).

1. Perform NAT settings on routers 0 and 3. Configure routing to the Internet and to the allocated ranges of public addresses.

1. Test the settings by pinging the "Internet address" from each node. View statistics and address translation: how many internal local IP addresses are listed in the sample output? How many internal global IP addresses are listed? How many port numbers are used in conjunction with internal global addresses? What will happen as a result of sending an echo request to the internal local address of the PC-A computer from the ISP's router? Why? **Note**: depending on the time elapsed since sending echo requests from each PC, you may not see all the conversions. ICMP conversions are characterized by low time limits.

1. Reconfigure NAT to match the internal list of source addresses and the pool of external addresses with congestion in NAT. View statistics and address translation: how many internal local IP addresses are listed in the sample output? How many internal global IP addresses are listed? How many port numbers are used in conjunction with internal global addresses?

1. Configure PAT for one address: according to the scenario of this part, the Internet provider assigned each company one IP address (for example, 11.11.11.11 and 13.13.13.13) for connecting to the Internet from routers 1 and 3.

1. Before configuring PAT for a single address, clear NAT translations and statistics from the router. Configure external and internal interfaces for NAT and ACL conversions. Translation between ACLs and the pool of external addresses should be deleted (no); pool of usable public addresses to delete. Configure the translation of access list addresses to the address of the router interface.

1. Test, map, and verify the implementation of conversions and analyze the NAT / PAT statistics to control the process.






