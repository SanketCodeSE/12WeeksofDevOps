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



