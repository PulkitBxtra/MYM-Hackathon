# My Detailed Approach to Setting Up a VPN Server in AWS Cloud

In the hackathon, I took on the challenge of setting up a VPN server in the AWS Cloud. To accomplish this, I followed a detailed technical approach that involved leveraging various AWS services, implementing specific configurations, and ensuring secure network communication. Here's a step-by-step breakdown of how I achieved the task:

## 1. Launching an EC2 Instance

To start, I accessed the AWS Management Console and navigated to the EC2 service. From there, I launched a new EC2 instance, carefully selecting an appropriate Amazon Machine Image (AMI) that included the OpenVPN software. This ensured that the necessary components for a VPN server were pre-installed on the instance. I also considered my requirements and opted for a suitable instance size, such as the "t2.micro" instance type, which is eligible for the AWS free tier.

## 2. Establishing SSH Connection

Once the EC2 instance was up and running, I established an SSH connection to the VPN server for further configuration. I retrieved the public IP address of the instance from the AWS Management Console. Then, using a terminal or command prompt, I initiated an SSH connection to the server by running the SSH command and providing the public IP address.

## 3. Configuring the VPN Server

With a successful SSH connection, I logged in as the "root" user on the VPN server. To perform the necessary configurations, I switched to the "openvpn" user. To ensure secure access, I made sure the "openvpn" user had a password set.

## 4. Accessing the Admin Portal

Returning to the AWS Management Console, I retrieved the VPN server's public IP address. Using this information, I accessed the Admin Portal of the VPN server through a web browser. As a security precaution, there might be warnings or certificate errors, which I accepted after verifying their legitimacy. Once past the initial security checks, I reached the login page of the Admin Portal.

I logged in using the "openvpn" username and the previously set password to gain access to the administrative controls and configurations.

## 5. Final Configuration and Client Setup

Within the Admin Portal, I navigated to the "Configuration" section and accessed the "VPN Settings." Here, I had various options to customize the VPN server based on my requirements. To enhance security and ensure all client internet traffic passes through the VPN, I enabled the appropriate option.

After making the necessary configuration adjustments, I saved the settings and updated the running server configuration. This ensured that the VPN server was properly configured to handle client connections and traffic routing.

To allow clients to connect to the VPN server, I proceeded to the User Portal. This portal can be accessed by removing "/admin" from the VPN server's URL. From there, I downloaded the OpenVPN client suitable for my device and operating system.

Once the client was downloaded, I installed it on my device and proceeded to configure the OpenVPN client using the downloaded profile. This involved specifying the necessary connection details, such as the VPN server's IP address or domain name, authentication credentials, and encryption settings.

Finally, with the OpenVPN client properly configured, I connected to the VPN server. This established a secure and private network connection, ensuring that my data was encrypted and transmitted through the VPN server.

By following this detailed technical approach, I successfully set up a VPN server in the AWS Cloud, providing secure and private network communication. This process involved careful consideration of AWS services, configurations, and client setup. I am proud of the solution I implemented during the hackathon, as it required a combination of technical skills and knowledge of AWS infrastructure.
