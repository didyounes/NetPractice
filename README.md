# 🌐 NetPractice - 42 Network

## 👤 Author
**Younes El Joulali (yel-joul)**
Student at 1337 Rabat (UM6P)

## 📝 Description
NetPractice is where the "magic" of the internet starts to make sense. Before this project, things like IP addresses and subnet masks felt like random numbers. This project changes that by turning networking into a series of 10 logical puzzles.

The goal is simple: make sure every computer and router in a given diagram can talk to each other. In practice, this means diving deep into the math of subnets and the logic of routing tables. By the end of Level 10, you stop seeing just numbers and start seeing how data actually finds its way across a global network.

> [!TIP]
> **Goal:** Fill in the blanks until all connection lines turn 🟢 Green. If they are 🔴 Red, check for configuration errors or "dead ends" in your routing.

## 🚀 Instructions

### How to Run the Training Interface
The project is entirely web-based. To get started:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yel-joul/netpractice.git
   ```
2. **Launch:** Open the `index.html` file in your browser (Chrome or Firefox work best).
3. **Select a level:** You’ll see a network diagram with several empty fields for IPs, masks, and gateways.

### Solving and Saving
- **Solve:** Adjust the IPs and masks until the network is fully connected.
- **Export:** When a level is solved, click the "Download" or "Export" button. This saves a small file containing your configuration.

### Submission Requirements
To complete the project, your repository must contain:
- 📁 **10 Configuration Files:** One for each level (e.g., `level1`, `level2`, etc.).
- 📄 **README:** This documentation.

## � Common Pitfalls & Troubleshooting
If you find yourself with 🔴 Red connection lines, check for these common errors:

- **Overlapping Subnets:** Ensure no two networks claim the same IP range. This often happens if a mask is too "wide" (e.g., using `/24` where `/25` is needed).
- **The "Return Trip":** Routing must work both ways. Just because Router A knows how to reach Router B, doesn't mean Router B knows how to reply. Check your routing tables on *both* sides.
- **Reserved IPs:** Remember that the first address (Network ID) and last address (Broadcast) in a subnet are often unusable for host assignment.
- **Gateway Confusion:** A client's "Default Gateway" must be the IP address of the router interface *directly connected* to that client's network link.

## �📚 Resources & Concepts Learned

### 📡 Core Networking Concepts
Through 10 levels of simulations, I mastered the fundamental rules that govern data transmission:

- **IPv4 Addressing:** Understanding the 32-bit structure of IP addresses and the distinction between the Network portion and the Host portion.
- **Subnetting & CIDR:**
  - Mastering CIDR notation (e.g., `/24`, `/30`).
  - Calculating Subnet Masks, Network Addresses, and Broadcast Addresses.
  - Determining the Valid Host Range (Subnet Size - 2).
- **Routing Logic:**
  - Configuring Routing Tables with destinations and Next-Hop addresses.
  - The role of the Default Gateway (`0.0.0.0/0`) as the exit point for local traffic.
- **Network Devices:**
  - **Switch:** Connects devices within the same subnet using MAC addresses (Layer 2).
  - **Router:** Forwards packets between different subnets (Layer 3).

### 🛠️ The OSI Model (Focus Layers)
This project focuses on the "Lower Stack" where the heavy lifting of data movement happens:

| Layer | Name | Protocol/Device | Key Function |
| :---: | :--- | :--- | :--- |
| **L4** | **Transport** | TCP / UDP | Ensures reliable data delivery and uses Ports. |
| **L3** | **Network** | IP / Routers | Manages logical addressing and Routing Path. |
| **L2** | **Data Link** | Ethernet / Switches | Node-to-node delivery and ARP (IP to MAC mapping). |
| **L1** | **Physical** | Cables / Hubs | Bit-stream transmission over physical media. |

## 🔗 Useful Resources

### 📖 Guides & Documentation
- **[Cisco - Introduction to Subnetting](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html):** The industry standard for technical networking documentation.
- **NetPractice Visual Guide (GitHub):** A comprehensive visual walkthrough specifically for the 42 project.
- **[RFC 1918](https://datatracker.ietf.org/doc/html/rfc1918):** The official standard for Private IP address ranges (`10.x`, `172.x`, `192.x`).

### 🕹️ Practice Tools
- **[Subnetting.net](https://www.subnetting.net/):** Great interactive games to improve your speed in calculating masks and host ranges.
- **[SubnetIPv4.com](https://subnetipv4.com/):** A random question generator to master the "Interesting Octet" method.
- **[Network Chuck - "You Suck at Subnetting"](https://www.youtube.com/playlist?list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF):** A high-energy video series that makes complex subnetting math very easy to understand.

---
*Created as part of the 42 curriculum.*