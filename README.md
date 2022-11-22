# Cisco Packet Tracer - Small Network

## Description

Cisco packet tracer is a networking simulation tool used to simulate and practice networking topics. In this project, I simulate the network of a small business that consists of three departments: human resources, marketing, and sales. I utilize various networking protocols and fundamentals to successfully route traffic
to and from end devices. Some of these protocols and fundamentals include router-rip, ssh, inter-vlan routing, trunk/access ports, and more.

## Walk-Through

#### Network Topology
This network topology consists of **three** PCs, **four** 2960 switches, **three** 4321 routers, and **one** server which will act as an ISP. The screenshot below also lists each device's respective IP.

<img src="https://user-images.githubusercontent.com/118637783/203377792-12c5ea71-f9f6-4898-8a15-f0e2213584aa.png" width="620" height="320">

#### Basic Configuration - PCs & Switches

- Each PC requires an assigned IP address, subnet mask, and default gateway. This configuration is straightforward.

- The switches need a bit more configuration. Each switch requires a hostname, some basic security (i.e. password/encryption), and a banner motd. Listed below are the commanads used to configure switch 1. 

![image](https://user-images.githubusercontent.com/118637783/203398716-5ed29926-16b6-44af-b16c-d3137bca3cac.png)

