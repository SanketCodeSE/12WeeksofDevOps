<h1>Task 1: Write examples of how each layer applies to real-world scenarios</h1>

<h2>OSI Model Example :</h2>

| **Layer**           | **Function**                                 | **Real-World Examples**                                                                                                                                                                            |
| ------------------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **7. Application**  | Interface between user and network services  | - **HTTP/HTTPS** for web browsing (e.g., visiting a website)<br>- **SMTP/IMAP** for email services (e.g., Gmail)<br>- **FTP** for file transfers                                                   |
| **6. Presentation** | Data translation, encryption, compression    | - **SSL/TLS encryption** (used in HTTPS for secure websites)<br>- **JPEG, MP4** file formats (data encoding/decoding)<br>- **Compression** tools (e.g., WinZip or video compression for streaming) |
| **5. Session**      | Manages sessions or connections between apps | - **Login sessions** on websites<br>- **VoIP calls** maintaining connection state<br>- **Remote desktop** sessions (RDP)                                                                           |
| **4. Transport**    | Reliable data transfer with error checking   | - **TCP** ensuring complete data delivery (e.g., loading a full webpage)<br>- **UDP** used in **video streaming**, **gaming**, or **VoIP** (less overhead)                                         |
| **3. Network**      | Determines path for data to travel           | - **IP (Internet Protocol)** addresses to route packets (e.g., sending a message to a remote server)<br>- **Routers** forwarding data based on destination IP                                      |
| **2. Data Link**    | Error detection and MAC addressing           | - **Ethernet/Wi-Fi** MAC addresses used in LAN communication<br>- **Switches** directing traffic based on MAC addresses                                                                            |
| **1. Physical**     | Transmits raw bits over medium               | - **Cables** (Ethernet, fiber)<br>- **Wi-Fi signals**<br>- **Network Interface Cards (NICs)**                                                                                                      |




<br><br><br>
<h2>TCP/Ip Model Example :</h2> 

| **TCP/IP Layer**          | **Equivalent OSI Layers** | **Real-World Examples**                                                                                                                            |
| ------------------------- | ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Application**           | OSI Layers 5–7            | - **HTTP, DNS, FTP, SMTP, SSH** (e.g., browsing, email, file transfers)                                                                            |
| **Transport**             | OSI Layer 4               | - **TCP** for reliable delivery (e.g., file download)<br>- **UDP** for fast but less reliable delivery (e.g., online games, live video)            |
| **Internet**              | OSI Layer 3               | - **IP** for addressing and routing<br>- **ICMP** used in **ping** to test connectivity                                                            |
| **Network Access / Link** | OSI Layers 1–2            | - **Ethernet** and **Wi-Fi** for physical delivery<br>- **ARP** for mapping IP addresses to MAC addresses<br>- **Switches and NICs** involved here |






<br><br><br>
<h2>Example: Streaming Music on Spotify </h2>

| **OSI Layer** | **What Happens**                                                                                  |
| ------------- | ------------------------------------------------------------------------------------------------- |
| Application   | The Spotify app sends a request to stream a song using its proprietary protocol over the internet |
| Presentation  | The audio is **decoded from Ogg Vorbis** format and decrypted                                     |
| Session       | Spotify maintains a session with the user account for playlist sync                               |
| Transport     | Data is delivered over **TCP** to ensure the stream is reliable                                   |
| Network       | **IP addresses** are used to route the stream from Spotify servers to your device                 |
| Data Link     | Your device communicates with the router via **MAC address**                                      |
| Physical      | Bits are transmitted via **Wi-Fi signals or mobile data**                                         |





<br><br><br><br><br>


<h1>Task 2: listing protocols and explaining their relevance to DevOps workflows.
</h1>
🔐 1. HTTP (HyperText Transfer Protocol)
Port: 80

Use in DevOps:
Accessing web servers (e.g., testing staging environments).
API communication between services during CI/CD.
Triggering webhooks in pipelines.
<br><br>

🔒 2. HTTPS (HTTP Secure)
Port: 443

Use in DevOps:
Securely accessing services over the web (e.g., GitHub, web dashboards).
Deploying secure web applications.
Enforcing TLS/SSL for production traffic.
<br><br>

📂 3. FTP (File Transfer Protocol)
Port: 21

Use in DevOps:
Transferring configuration files or artifacts (used less often now).
Legacy systems or devices that still rely on FTP for deployment.
⚠️ Often replaced by more secure alternatives like SFTP or HTTPS-based uploads.
<br><br>

🔑 4. SSH (Secure Shell)
Port: 22

Use in DevOps:
Remote access to Linux/Unix servers.
Automating tasks via scripts (Ansible, Fabric, etc.).
Git operations over SSH (e.g., git@github.com:user/repo.git).
Securing CI/CD agents or bastion hosts.
<br><br>

🌐 5. DNS (Domain Name System)
Port: 53 (UDP and TCP)

Use in DevOps:
Resolving domain names to IPs in infrastructure provisioning.
Managing custom DNS entries for internal environments.
Debugging name resolution issues (e.g., with dig, nslookup).



<br><br><br><br><br>
<h1>Task: Write a step-by-step guide on how to create and configure Security Groups.</h1>


🔐 What is a Security Group?
A Security Group in AWS acts as a virtual firewall that controls inbound and outbound traffic to your EC2 instances and other resources.
<br><br>
<h3>Step to create and configure Security Groups. </h3>
🧩 Step 1: Log in to AWS Console
Go to: https://console.aws.amazon.com
Sign in with your IAM or root credentials.
<br><br>

🔧 Step 2: Navigate to EC2 Dashboard
In the AWS Management Console, search for EC2 in the search bar and click EC2.
On the left sidebar, scroll down and click Security Groups under Network & Security.
<br><br>

➕ Step 3: Create a New Security Group
Click the “Create security group” button.
Fill in the following:
Security group name: e.g., web-server-sg
Description: e.g., Allow HTTP, HTTPS, and SSH
VPC: Choose the appropriate VPC (usually default if you're unsure)
<br><br>

🔐 Step 4: Configure Inbound Rules
Click “Add Rule” for each type of traffic you want to allow.
Type	Protocol	Port Range	Source
SSH	TCP	22	My IP (for secure admin access)
HTTP	TCP	80	0.0.0.0/0 (public web access)
HTTPS	TCP	443	0.0.0.0/0 (secure web access)
💡 Tip: Avoid opening SSH (22) to 0.0.0.0/0 in production.
<br><br>

📤 Step 5: Configure Outbound Rules (Optional)
By default, all outbound traffic is allowed.
You can restrict this if needed (e.g., block external internet access).
<br><br>

🧱 Step 6: Review and Create
Double-check your settings and click “Create security group”.
<br><br>

🔗 Step 7: Attach Security Group to an EC2 Instance
Go to EC2 Instances.
Select your instance → Click Actions > Security > Change security groups.
Select your new security group (web-server-sg) and click Apply.
<br><br>

🧪 Step 8: Test Your Configuration
Try connecting via SSH (ssh ec2-user@your-ec2-ip)
Visit your public IP in a browser to check HTTP/HTTPS access.


<br><br><br><br><br>
<h1>Task 4: Create a cheat sheet explaining the purpose and usage of each command.</h1>

🧠 Networking Commands Cheat Sheet:

🔄 1. ping – Check Connectivity

Purpose:Tests if a host is reachable and measures round-trip time.
<br><br>
🛣️ 2. traceroute / tracert – Trace Packet Path

Purpose:Shows the path (hops) packets take from your machine to a destination.
<br><br>
📊 3. netstat – Network Statistics

Purpose:Displays network connections, listening ports, routing tables, and more.
<br><br>
🌐 4. curl – Make HTTP(S) Requests

Purpose:Transfers data to/from a server using protocols like HTTP, HTTPS, FTP, etc.
<br><br>
🌍 5. dig / nslookup – DNS Lookup Tools
🔍 dig (Linux/macOS)

Purpose: Query DNS servers for information about hostnames.
<br><br>
🔍 6. nslookup (Windows/Linux)

Purpose: Interactively query DNS to resolve hostnames.




