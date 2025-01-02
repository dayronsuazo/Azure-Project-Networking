# Azure-Project-Networking
Setting Up a Virtual Network and Connect VMs (Networking)

Objective

The primary objective of this project is to set up a secure and interconnected virtual network in Azure, enabling seamless internal communication between virtual machines (VMs). This involves creating a virtual network, deploying VMs within the same network and subnet, configuring network security groups (NSGs) for secure communication and testing connectivity between the VMs.

For example
Job Specific Scenario - Setting Up a Private Development Environment

I was tasked with creating a secure, isolated environment for developers to test and deploy their applications. The goal is to provide developers with two VMs where they can collaborate on application testing without exposing the environment to the public internet.

Steps taken:

Virtual Network Creation: create a virtual network (my-vnet) to isolate the development environment. This ensures all resources in the network can communicate privately and securely.
Deploying VMs: Two VMs are created within the same virtual network and subnet. For instance:
VM1 hosts the development server (e.g., application backend).
VM2 serves as a database server.

Internal Communication Setup:
NSGs are configured to allow communication between the VMs on specific ports:
Port 22 for SSH (Linux) or 3389 for RDP (Windows) for admin access.
Custom ports for application and database communication, such as port 3306 for MySQL.

Testing Connectivity: Verify the setup by SSHing into VM1 and pinging VM2 to confirm the private IP-based communication.

Outcome:
Developers can securely access the VMs, deploy code and test applications.
The VMs communicate internally without exposing sensitive services to the internet, reducing the risk of unauthorised access.
The environment can scale later by adding more VMs or services within the same virtual network.

This type of setup is common when creating development, testing or staging environments that mimic production configurations while ensuring security and cost efficiency.
