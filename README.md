# EXPT NO.3 IMPLEMENTATION OF LINK STATE ROUTING PROTOCOL OSPF
# AIM

To connect computers in multiple networks using Open Shortest Path First Routing Protocol and to verify the connectivity between computers.

# EQUIPMENTS REQUIRED
Desktop Computer
Cisco Packet Tracer 5.0 Software

# IP ASSIGNMENT
<img width="829" height="519" alt="image" src="https://github.com/user-attachments/assets/277f8414-8287-4c25-8bb0-77fae0138626" />

# NETWORK DIAGRAM
<img width="678" height="468" alt="image" src="https://github.com/user-attachments/assets/68d78cb6-f19e-47e7-b67f-7319314f87c9" />



# PROCEDURE
STEP 1: Open a Packet Tracer Software.
STEP 2: Drag two 2900 Switches, two Cisco 1800 Routers, four PC Terminals from tool bar and drop it in work area.
STEP 3: Connect all the PC Terminals and Routers through Switches as shown in the network diagram using CAT 6 Patch cables.
STEP 4: Configure IP address and Gateway in all PC Terminals.
STEP 5: Configure Delhi router IP address, save configuration and restart Delhi router. STEP 6: Configure Chennai router IP address, save configuration and restart Chennai router. STEP 7: Check the connectivity between the computers in network.
STEP 8: Configure OSPF in Delhi router, Save configuration and restart Delhi router.
STEP 9: Configure OSPF in Chennai router, Save configuration and restart Chennai router.
STEP 10: Verify the connectivity between PC Terminals in different networks using Ping command.
STEP 11: Check the routing table in Delhi router and Chennai router using show ip route command
# Router 0 Program
Router0> enable 
Router0# configure terminal 
Router0(config)# interface FastEthernet0/0 
Router0(config-if)# ip address 192.168.1.1 255.255.255.0 
Router0(config-if)# no shutdown 
Router0(config-if)# exit 
Router0(config)# interface Serial2/0 
Router0(config-if)# ip address 192.168.2.1 255.255.255.0 
Router0(config-if)# clock rate 64000 
Router0(config-if)# no shutdown 
Router0(config-if)# exit 
Router0(config)# router ospf 1 
Router0(config-router)# router-id 1.1.1.1 
Router0(config-router)# network 192.168.1.0 0.0.0.255 area 0 
Router0(config-router)# network 192.168.2.0 0.0.0.255 area 0 
Router0(config-router)# exit 
Router0# write memory
# Router 1 Program
Router1> enable 
Router1# configure terminal 
Router1(config)# interface FastEthernet0/0 
Router1(config-if)# ip address 192.168.3.1 255.255.255.0 
Router1(config-if)# no shutdown 
Router1(config-if)# exit 
Router1(config)# interface Serial2/0 
Router1(config-if)# ip address 192.168.2.2 255.255.255.0 
Router1(config-if)# no shutdown 
Router1(config-if)# exit 
Router1(config)# router ospf 1 
Router1(config-router)# router-id 2.2.2.2 
Router1(config-router)# network 192.168.3.0 0.0.0.255 area 0 
Router1(config-router)# network 192.168.2.0 0.0.0.255 area 0 
Router1(config-router)# exit 
Router1# write memory

# OUTPUT
<img width="1161" height="462" alt="image" src="https://github.com/user-attachments/assets/84f75b6b-4a1f-460b-8ba7-3f8c28301063" />

<img width="755" height="349" alt="image" src="https://github.com/user-attachments/assets/c290779b-0226-42d5-92f1-60061c9161b8" />



# RESULT
Thus the computers in multiple networks using Open Shortest Path First Routing Protocol is connected and the connectivity between the computers is verified.

