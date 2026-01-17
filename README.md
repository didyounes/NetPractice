*This project has been created as part of the 42 curriculum by yel-joul.*

# NetPractice

Description
NetPractice is where the "magic" of the internet starts to make sense. Before this project, things like IP addresses and subnet masks felt like random numbers. This project changes that by turning networking into a series of 10 logical puzzles.

The goal is simple: make sure every computer and router in a given diagram can talk to each other. In practice, this means diving deep into the math of subnets and the logic of routing tables. By the end of Level 10, you stop seeing just numbers and start seeing how data actually finds its way across a global network.

Instructions
How to Run the Training Interface
The project is entirely web-based. To get started:

Clone this repository.

Open the index.html file in your browser (Chrome or Firefox work best).

Select a level: You’ll see a network diagram with several empty fields for IPs, masks, and gateways.

Solving and Saving
The Goal: Fill in the blanks until all the connection lines turn green. If they are red, there is a configuration error or a "dead end" in your routing.

Exporting: When a level is solved, click the "Download" or "Export" button. This saves a small file containing your configuration.

Submission Requirements
To complete the project, your repository must contain:

10 Configuration Files: One for each level (e.g., level_1, level_2, etc.), placed at the root of the folder.

The README: You're looking at it!

Resources
Networking Concepts I Learned
Completing these levels required me to master several concepts that are usually invisible to the average user:

1. The OSI Model
The Open Systems Interconnection (OSI) model conceptualizes how networks operate. While there are 7 layers, this project focuses heavily on the bottom layers that control data transport:

Layer 1 (Physical): The physical cables and hardware which transmit the raw bit stream.
Layer 2 (Data Link): Where Switches operate. This layer handles node-to-node delivery on the same local network using MAC addresses to ensure frames reach the correct device.
Layer 3 (Network): The core of this project. Routers operate here using IP addresses to packetize data and route it across different networks (Subnets) to reach its destination.
Layer 4 (Transport): Manages reliability and data streams using Ports (e.g., TCP/UDP), ensuring data reaches the correct application (like a web server or SSH daemon).

2. IP Addressing & Subnetting
IPv4 Structure: Learning the difference between the "Network" part of an address and the "Host" part.

Subnet Masks (CIDR): Mastering notations like /24 or /30. This project teaches you that a mask isn't just a number—it’s a boundary that defines how many devices can exist on a network.

Default Gateway: Learning that the Gateway is basically the "Exit Door" for a network. Without it, your data is stuck in the local room.

3. Routing Tables
This was the most challenging part of the later levels. I had to learn how to tell a router: "If you want to reach Network A, send the data to Router B."

### Useful Links

Subnetting.net - Great for practicing the math.

Cisco's Guide to Subnetting - The "Gold Standard" for technical documentation.

### AI Usage
I used AI assistance to verify my understanding of specific networking concepts (such as the mathematical calculations for subnet masks and the logic behind complex routing tables) and to help explain the layers of the OSI model.
