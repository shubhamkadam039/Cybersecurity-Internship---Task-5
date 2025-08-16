# Cybersecurity-Internship---Task-5
Task : Network Packet Capture and Analysis using Wireshark

## Objectives

- Install and configure Wireshark for packet capture
- Capture live network packets from active interface
- Identify and analyze at least 3 different network protocols
- Generate network traffic through web browsing and network commands
- Export captured data as .pcap file
- Document findings in a comprehensive analysis report

## Tools and Environment

| Tool             | Version | Purpose                          |
|------------------|---------|----------------------------------|
| **Wireshark**    | 4.4.8   | Network packet capture and analysis |
| **Operating System** | Windows x64 | Host environment for packet capture |
| **Network Interface** | Wifi | Active interface for traffic capture |

## Capture Summary

### Basic Statistics
- **Total Packets Captured**: 24389
- **Capture Duration**: 07:07 mins
- **Average Packet Size**: 682
- **Network Interface**: Wifi
- **Capture Filter**: None (captured all traffic)

### Traffic Generation Methods
1. **Web Browsing**: Visited multiple websites (google.com, github.com, etc.)
2. **DNS Queries**: Used `nslookup` and `ping` commands
3. **Background Applications**: Normal system network activity

## Protocol Analysis

### Protocols Identified

#### 1. TCP (Transmission Control Protocol)
- **Port Numbers**: Various (80, 443, 22, etc.)
- **Packet Count**: 17786
- **Percentage**: 100%
- **Key Characteristics**:
  - Connection-oriented protocol
  - Three-way handshake observed
  - Reliable data transmission
  - Flow control mechanisms

#### 2. HTTP (Hypertext Transfer Protocol)
- **Port Number**: 80
- **Packet Count**: [Count from analysis]
- **Purpose**: Web page requests and responses
- **Observations**:
  - GET requests to various domains
  - Response codes (200, 404, etc.)
  - Clear text protocol (visible content)

#### 3. HTTPS/TLS (Secure HTTP)
- **Port Number**: 443
- **Packet Count**: [Count from analysis]
- **Purpose**: Encrypted web communication
- **Observations**:
  - TLS handshake sequences
  - Encrypted application data
  - Certificate exchanges

#### 4. DNS (Domain Name System)
- **Port Number**: 53 (UDP)
- **Packet Count**: 446
- **Purpose**: Domain name resolution
- **Observations**:
  - A record queries
  - Response with IP addresses
  - Query-response pairs

#### 5. UDP (User Datagram Protocol)
- **Various Ports**: 53, 123, etc.
- **Purpose**: Fast, connectionless transport
- **Observations**:
  - No connection establishment
  - Lower overhead than TCP
  - Used for DNS and other services

#### 6. ICMP (Internet Control Message Protocol)3
- **Purpose**: Network diagnostics
- **Observations**:
  - Ping echo requests/replies
  - Network reachability testing
  - Error message reporting

## Key Findings

### Traffic Patterns
- **Most Active Protocol**: TCP
- **Primary Communication**: Web browsing traffic (HTTP/HTTPS)
- **DNS Activity**: Frequent domain resolution queries
- **Security Observations**: Mix of encrypted and unencrypted traffic

### Network Behavior
- **Peak Traffic**: During web browsing activities
- **Connection Patterns**: Multiple concurrent TCP connections
- **Protocol Distribution**: Predominantly TCP-based protocols
- **Background Activity**: System maintenance and update traffic

### Interesting Observations
1. **TLS Encryption**: Most web traffic is encrypted (HTTPS)
2. **DNS Queries**: Frequent lookups for domain resolution
3. **Keep-Alive Connections**: HTTP persistent connections observed
4. **Port Usage**: Standard ports (80, 443, 53) heavily utilized

## Wireshark Display Filters Used

| Filter              | Purpose                        | Example                |
|---------------------|-------------------------------|------------------------|
| `http`              | Show HTTP traffic only         | Web requests/responses |
| `dns`               | Show DNS queries/responses     | Domain name lookups    |
| `tcp.port == 443`   | Show HTTPS traffic             | Secure web connections |
| `ip.addr == 192.168.1.1` | Show traffic to/from specific IP | Router communication   |
| `icmp`              | Show ping/diagnostics          | Network tests          |
   
## Learning Outcomes

### Technical Skills Gained
- **Network Protocol Understanding**: Deep dive into TCP/IP stack
- **Packet Analysis**: Ability to interpret network traffic
- **Security Awareness**: Understanding of encrypted vs. unencrypted traffic
- **Troubleshooting Skills**: Network diagnostics and problem identification

### Cybersecurity Insights
- **Traffic Monitoring**: Importance of network visibility
- **Protocol Security**: Vulnerabilities in plain text protocols
- **Network Forensics**: Using packet analysis for incident response
- **Baseline Understanding**: Normal vs. suspicious network behavior

## Security and Privacy Considerations

⚠**Important Note**: This packet capture was performed on a personal network with proper authorization. No sensitive or personal data from other users was captured or analyzed. All analysis was conducted in accordance with ethical hacking principles and local regulations.

### Best Practices Followed
- Only captured traffic on owned/authorized networks
- No interception of other users' private communications
- Secure storage of capture files
- No sharing of sensitive network information

## Interview Preparation

**1. What is Wireshark used for?**  
Wireshark is a network protocol analyzer. It is used to capture, inspect, and analyze network traffic in real time for troubleshooting, education, security monitoring, and protocol development.

**2. What is a packet?**  
A packet is a basic unit of data sent across networks. It contains control information (headers) and the payload (actual data), allowing communication between devices using various protocols.

**3. How to filter packets in Wireshark?**  
In Wireshark, you can filter packets using the display filter bar. Examples:
- `http` — Shows only HTTP packets  
- `dns` — Shows only DNS queries and responses  
- `tcp` or `udp` — Filters by protocol  
You can also use logical operators (`and`, `or`, `not`) for advanced filtering.

**4. What is the difference between TCP and UDP?**  
- **TCP** is connection-oriented, reliable, and ensures data arrives in order; it uses error correction and acknowledgments.
- **UDP** is connectionless, faster, but doesn’t guarantee delivery or order; it has lower overhead and is suitable for real-time applications.

**5. What is a DNS query packet?**  
A DNS query packet is a request sent to a DNS server to resolve a domain name (like www.example.com) into its IP address. It usually uses UDP port 53.

**6. How can packet capture help in troubleshooting?**  
Packet capture reveals exactly what’s happening on the network, allowing you to identify problems such as dropped packets, delays, misconfigured devices, or malicious activities by analyzing live traffic.

**7. What is a protocol?**  
A protocol is a standardized set of rules that specifies how data is formatted, transmitted, and received in a network. Examples include TCP, UDP, HTTP, DNS, etc.

**8. Can Wireshark decrypt encrypted traffic?**  
Wireshark cannot decrypt encrypted traffic (like HTTPS/TLS) unless you provide the necessary decryption keys. Without them, you can only analyze metadata or handshake information, not the encrypted content itself.

***

## 🔗 Additional Resources

- [Wireshark Official Documentation](https://www.wireshark.org/docs/)
- [Network Protocol Fundamentals](https://www.cloudflare.com/learning/network-layer/)
- [Packet Analysis Best Practices](https://wiki.wireshark.org/PacketAnalysis)

***
