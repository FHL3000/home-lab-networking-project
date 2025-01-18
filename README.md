# Home Lab Networking Project

## Overview
This repository documents the design, setup, and configuration of my home lab. The project is aimed at gaining hands-on IT experience in networking, DNS management, and security using a Raspberry Pi, Pi-hole, and a subnet configuration.

### Finished Home Lab
Below is the final setup of my home lab environment.

![Finished Home Lab](./images/Finished-Home-Lab.JPG)


## Objectives
- Create a secure, isolated sub-network for IT experimentation.
- Gain practical experience with network setup, configuration, and troubleshooting.
- Explore advanced tools like Pi-hole for DNS management and traffic monitoring.

## Equipment
- Raspberry Pi 5 with active and passive cooling case
- ASUS RT-AX3000 WIFI 6 Router
- NETGEAR 8-Port Gigabit Switch
- Logitech K400 Keyboard
- VGA to Micro HDMI Adapter
- 100 ft Flat Ethernet Cat6 Cable & Patch cables
- Ethernet Wall Plate(s)
- Back-UPS999

## Configurations
- **Subnet**: 10.0.0.0/24
- **Static IPs**: Assigned for key devices like Raspberry Pi and laptop.
- **DHCP Range**: 10.0.0.50 - 10.0.0.200.
- **Firewall Rules**: Configured UFW on the Raspberry Pi.
- **Pi-hole Integration**: DNS filtering and traffic monitoring.

## Network Diagram
Below is a visual representation of the network setup.

![Network Diagram](./images/Homelab-Network-Diagram.jpg)

## Ethernet Layout Blueprint
Below is the basic blueprint of the Ethernet cable routing throughout the home.

![Ethernet Layout Blueprint](./images/Basic-Blueprint-Ethernet-Layout.png) 


## Logs
- [Ping Test Results](./logs/ping-test-results.log)
- [Traceroute Results](./logs/traceroute-test.log)
- [Pi-hole DNS Queries](./logs/pihole-dns-queries.log)

## Configurations
- [Router Configuration](./configs/router-config.txt)
- [DHCP Settings](./configs/dhcp-settings.txt)
- [Firewall Rules](./configs/ufw-rules.txt)
- [Pi-hole Blocklist](./configs/pihole-blocklist.txt)

## Challenges and Solutions
Throughout the project, I encountered several challenges that required creative problem-solving. Here are some examples:

### Challenge 1: Routing Ethernet Cables
- **Problem**: Extending an Ethernet cable discreetly from the ISP router in one room to the secondary router in another room while avoiding visible wires.
- **Solution**: Used cable fish tape to run the Ethernet cable through interior walls, routing it via the attic and exiting cleanly into the home lab room.

### Challenge 2: DNS Configuration Issues
- **Problem**: Pi-hole was not resolving DNS queries correctly, causing intermittent connectivity issues.
- **Solution**: Verified and corrected the DNS servers and `/etc/resolv.conf` file. Restarted the DNS service and tested functionality with `ping` and `nslookup`.

### Challenge 3: Packet Loss
- **Problem**: Initial tests showed up to 10% packet loss when pinging the Raspberry Pi from other devices.
- **Solution**: Identified DNS misconfigurations as the root cause and resolved the issue by updating Pi-hole settings and restarting network services.

### Challenge 4: Accessing the Router’s Web Interface
- **Problem**: Could not access the router's web interface using `router.asus.com`.
- **Solution**: Proper DNS configuration resolved DNS resolution issues.

## Skills Gained
- Subnetting and IP management.
- Configuring DHCP, DNS, and firewalls.
- Hands-on experience with Pi-hole and Raspberry Pi.
- Network troubleshooting and performance optimization.

## Future Plans
- Implement VLANs for additional network segmentation.
- Explore automated monitoring tools.
- Expand the lab with cloud-based integrations.
- Further advanced network configuration and penetration testing

## Contact
Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/kendric-cuthbertson-9626b5210/) or explore more of my projects on GitHub

## Gallery
Below are images and a video showcasing various stages of the project. For additional setup images, visit the [images/](./images/) folder in this repository.

### Faceplate Installation
1. **Measuring for Faceplate Installation**  
   ![Faceplate Measurements](./images/Faceplate-measurments.JPG)

2. **Cutting the Faceplate Opening**  
   ![Faceplate Cutout](./images/Faceplate-cutout.JPG)

3. **Horizontal Cable Run**  
   ![Horizontal Run](./images/Horizonatal-Run.JPG)

4. **Finished Faceplate Installation**  
   ![Finished Faceplate Install](./images/Finished-Faceplate-Install.JPG)

### Device Rack Setup
5. **Repurposed Device Rack with LED Lighting**  
   ![Repurposed Device Rack](./images/Repurposed-Device-Rack.JPG)

### DNS Troubleshooting
6. **Initial DNS Loop Problem**  
   ![DNS Loop Problem](./images/DNS-Loop-Problem.JPG)

7. **Resolved DNS Loop Issue**  
   ![DNS Loop Resolved](./images/DNS-Loop-Resolved.JPG)


For more detailed visuals, check out the [images/](./images/) folder.
