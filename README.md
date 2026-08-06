# E-Commerce Data Center Network Simulation

A computer-network simulation developed in Cisco Packet Tracer for an e-commerce organization.

The topology separates different organizational teams and services into five `/24` networks. It includes web, administration, support, data-center, and wireless zones connected through switches and a central router.

## Network Topology

![E-Commerce Data Center Network](screenshots/network-topology.png)

## Project Objectives

* Design a network for an e-commerce organization
* Divide departments into separate IP networks
* Assign static IP addresses and default gateways
* Connect multiple wired and wireless devices
* Provide centralized DNS, web, and mail server roles
* Include a RADIUS server in the wireless zone
* Practise network configuration using Cisco Packet Tracer
* Test communication between devices and network blocks

## Network Design

The organization is divided into the following blocks:

| Block   | Department or purpose | Network           | Default gateway |
| ------- | --------------------- | ----------------- | --------------- |
| Block A | Web Team              | `192.168.10.0/24` | `192.168.10.1`  |
| Block B | Admin Team            | `192.168.20.0/24` | `192.168.20.1`  |
| Block C | Support Team          | `192.168.30.0/24` | `192.168.30.1`  |
| Block D | Data Center           | `192.168.99.0/24` | `192.168.99.1`  |
| Block E | Wi-Fi Zone            | `192.168.40.0/24` | `192.168.40.1`  |

The `/24` subnet mask used by each network is:

```text
255.255.255.0
```

## IP Addressing Plan

### Block A — Web Team

| Device | IP address     |
| ------ | -------------- |
| PC0    | `192.168.10.2` |
| PC1    | `192.168.10.3` |
| PC2    | `192.168.10.4` |

### Block B — Admin Team

| Device | IP address     |
| ------ | -------------- |
| PC3    | `192.168.20.2` |
| PC4    | `192.168.20.3` |

### Block C — Support Team

| Device  | IP address     |
| ------- | -------------- |
| PC5     | `192.168.30.2` |
| PC8     | `192.168.30.3` |
| PC7     | `192.168.30.4` |
| Laptop1 | `192.168.30.5` |
| Laptop0 | `192.168.30.6` |

### Block D — Data Center

| Server      | IP address     | Purpose                       |
| ----------- | -------------- | ----------------------------- |
| DNS Server  | `192.168.99.2` | Domain-name resolution        |
| Web Server  | `192.168.99.3` | E-commerce web services       |
| Mail Server | `192.168.99.4` | Organizational email services |

### Block E — Wi-Fi Zone

| Device        | IP address     | Purpose                 |
| ------------- | -------------- | ----------------------- |
| Laptop2       | `192.168.40.2` | Wireless client         |
| RADIUS Server | `192.168.40.3` | Wireless authentication |
| Laptop3       | `192.168.40.4` | Wireless client         |

## Network Components

The simulation contains:

* One Cisco 2901 router
* Two Cisco 2960-24TT switches
* One WRT300N wireless router
* Desktop computers for web, admin, and support teams
* Wired and wireless laptops
* DNS server
* Web server
* Mail server
* RADIUS server

## Networking Concepts Demonstrated

* IPv4 addressing
* `/24` subnetting
* Default-gateway configuration
* Multiple network segments
* Wired LAN connectivity
* Wireless network connectivity
* Router and switch integration
* Client-server architecture
* DNS, web, and email server roles
* Centralized wireless authentication
* Network simulation and troubleshooting

## How to Open the Project

### Requirements

Install Cisco Packet Tracer on your computer.

### Instructions

1. Download or clone this repository.
2. Open Cisco Packet Tracer.
3. Select **File → Open**.
4. Open:

```text
ecommerce-data-center-simulation.pkt
```

5. Allow the topology to load.
6. Inspect device configurations and use Simulation Mode to observe network traffic.

## Suggested Testing

The following tests can be performed inside Packet Tracer:

### Test Local Connectivity

Open a PC’s command prompt and ping another device in the same network:

```text
ping 192.168.10.3
```

### Test Data Center Connectivity

From a client device, test communication with the servers:

```text
ping 192.168.99.2
ping 192.168.99.3
ping 192.168.99.4
```

### Test Communication Between Networks

Ping a device in another organizational block:

```text
ping 192.168.20.2
```

### Test Wireless Connectivity

Use a wireless laptop to verify its connection with the WRT300N wireless router and other permitted devices.

### Use Simulation Mode

Packet Tracer’s Simulation Mode can be used to:

* Create a Simple PDU
* Observe packet movement
* Inspect ARP and ICMP traffic
* Identify successful or failed communication
* Troubleshoot addressing and gateway problems

## Project Files

```text
ecommerce-data-center-network/
├── README.md
├── ecommerce-data-center-simulation.pkt
├── screenshots/
│   └── network-topology.png
└── LICENSE
```

## Current Limitations

* This is a simulated network and does not use physical equipment.
* The topology represents a small academic e-commerce environment.
* Performance, security, and redundancy are limited compared with a production data center.
* Advanced features should only be listed after they have been configured and tested.

## Future Improvements

* Add VLANs for departmental separation
* Configure access-control lists
* Add DHCP services
* Implement a firewall
* Add redundant routers and switches
* Configure dynamic routing
* Add network monitoring
* Create a guest wireless network
* Add VPN-based remote access
* Introduce server and link redundancy

## What I Learned

This project improved my understanding of network topology design, IPv4 addressing, default gateways, routers, switches, server roles, wireless networking, and testing connectivity in Cisco Packet Tracer.

It also helped me understand how an organization can separate its departments while providing access to centralized data-center services.

## Project Information

* **Project type:** Computer Networks lab project
* **Simulation tool:** Cisco Packet Tracer
* **Network type:** E-commerce organizational network
* **Status:** Completed

## Author

**Talal Nasir**
Computer Science Student

## Disclaimer

This project was created for educational purposes. The network represents a simulated academic environment rather than a production-ready data center.
