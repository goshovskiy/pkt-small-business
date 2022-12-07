# Cisco Packet Tracer - Small Network [in-progress]

## Description

Cisco packet tracer is a networking simulation tool used to simulate and practice networking topics. In this project, I simulate the network of a small business that consists of three departments: human resources, marketing, and sales. I utilize various networking protocols and fundamentals to successfully route traffic
to and from end devices. Some of these protocols and fundamentals include router-rip, ssh, inter-vlan routing, and trunk/access ports.

## Walk-Through

#### Network Topology
This network topology consists of **three** PCs, **four** 2960 switches, **three** 4321 routers, and **one** server which will act as an ISP. The screenshot below also lists each device's respective IP.

<img src="https://user-images.githubusercontent.com/118637783/203377792-12c5ea71-f9f6-4898-8a15-f0e2213584aa.png" width="620" height="320">

#### Basic Configuration - PCs, Switches, & Routers

- Each PC requires an assigned IP address, subnet mask, and default gateway. This configuration is straightforward.

- The switches need a bit more configuration. Each switch requires a hostname, some basic security (i.e. password/encryption), and a banner motd. Listed below are the commanads used to configure switch 1. 

  -![image](https://user-images.githubusercontent.com/118637783/203398716-5ed29926-16b6-44af-b16c-d3137bca3cac.png)
   #### Breakdown:
   - enable secret _password_ - enables a password and password encryption that's based on the md5 hashing algorithm.
   - line console 0 - provides configuration access for the console port.
     - password _password_ - sets a password on the console port.
     - login - controls and prompts the user login request.
   - line vty 0 15 - provides configuration access for all 16 virtual lines that allow connecting to the device using telnet or SSH.
     - password _password_ - sets a password on the console port.
     - login - controls and prompts the user login request.
   - service password-encryption - encrypts all the passwords in running-config it can find, including enable password.
   - banner motd $ $ - configures a banner and message of the day.

- Routers receive a very similar configuration, only difference being the number of vty lines that can be configured (by default routers only have 5).
  
  -![image](https://user-images.githubusercontent.com/118637783/203839577-b89e975d-6def-4ba0-b984-9c6e956728f4.png)

- We need to assign an IP on a VLAN to each switch. Also, we must assign IPs on the respective interfaces to every router. I will begin explaining the steps in the next section: Switches and Routers - IP configuration.

#### Switches and Routers - VLAN/IP Configuration

- To begin, we'll start with the switches.

  -![image](https://user-images.githubusercontent.com/118637783/203892484-b5e2de4d-34a1-43c7-a388-a2585e14edc3.png)
  
  -![image](https://user-images.githubusercontent.com/118637783/204661881-a7925171-c8c9-4ccd-8a7b-ecdf3a613d9c.png)
  
  -![image](https://user-images.githubusercontent.com/118637783/204662189-c233280b-f8e7-435e-ab0f-e379153b869c.png)
  
  -![image](https://user-images.githubusercontent.com/118637783/204671079-30f57c87-55fe-4050-90a2-7dab246f0353.png)

- Now, the routers.

  -![image](https://user-images.githubusercontent.com/118637783/204663361-5b3650eb-c601-47b8-b845-dcc5877dd125.png)
  
  -![image](https://user-images.githubusercontent.com/118637783/204663989-7116a93d-0391-4a57-b2ad-c0ad38b95c9c.png)
  
  -![image](https://user-images.githubusercontent.com/118637783/204670015-d6843b7d-126d-4896-8aa9-f11cf352dd46.png)
 
 
#### Trunk Configuration

- We setup access ports on our switches, now we need to setup trunks to carry traffic across all VLANs.

  -




#### Inter-VLAN Routing - Router-on-a-Stick

- Router-on-a-stick:

  -![image](https://user-images.githubusercontent.com/118637783/204670908-3f412a99-154a-44e8-b685-a23748459516.png)
  
  -![image](https://user-images.githubusercontent.com/118637783/204671790-32bd7a9f-4ed5-4f96-bcd5-495cab41abd1.png)






