# **Task 5 – Wireshark Packet Capture & Network Traffic Analysis**

## **1. Objective**

The purpose of this task is to capture and analyze live network packets using Wireshark, apply protocol filters, identify the types of traffic flowing in the network, and understand how packet analysis supports cybersecurity and network troubleshooting.

---

## **2. Tools Used**

| Tool                      | Purpose                                  |
| ------------------------- | ---------------------------------------- |
| **Wireshark**             | Packet capturing and protocol analysis   |
| **Web Browser**           | To generate network traffic (HTTPS, DNS) |
| **Command Prompt – Ping** | To generate ICMP packets                 |

---

## **3. Packet Capture Overview**

A 1-minute packet capture session was performed while browsing the internet and pinging a public server. The captured `.pcap` file contained multiple network communication protocols.

### **Protocols Identified**

| Protocol  | Description                       | Purpose in Communication                          |
| --------- | --------------------------------- | ------------------------------------------------- |
| **TCP**   | Transmission Control Protocol     | Reliable, connection-oriented data transfer       |
| **UDP**   | User Datagram Protocol            | Fast, connection-less delivery used for streaming |
| **DNS**   | Domain Name System                | Resolves domain names to IP addresses             |
| **HTTPS** | Secure Hypertext Protocol         | Encrypted secure web browsing                     |
| **ICMP**  | Internet Control Message Protocol | Network reachability test (ping)                  |

---

## **4. Filters Applied in Wireshark**

| Protocol | Filter Applied |
| -------- | -------------- |
| TCP      | `tcp`          |
| UDP      | `udp`          |
| DNS      | `dns`          |
| HTTPS    | `tls` or `ssl` |
| ICMP     | `icmp`         |

Filters helped isolate protocol traffic to view packet-level details.

---

## **5. Detailed Observations**

| Protocol | Example Packet Observation      | Interpretation                                     |
| -------- | ------------------------------- | -------------------------------------------------- |
| DNS      | Standard Query `A → google.com` | System requested the IP address of google.com      |
| TCP      | `SYN → SYN/ACK → ACK` handshake | New connection established between client & server |
| HTTPS    | TLS Client Hello / Server Hello | Secure encrypted communication initiated           |
| UDP      | Packets with no acknowledgment  | Connection-less fast network delivery              |
| ICMP     | Echo Request & Echo Reply       | Ping testing for device/network reachability       |

---

## **6. Why Packet Capture Matters in Cybersecurity**

Packet capture helps in:

* Identifying suspicious network traffic
* Detecting malware communication
* Troubleshooting network performance issues
* Analyzing port scanning attempts
* Confirming encrypted vs unencrypted traffic

Wireshark is often used by security analysts, network engineers, and incident responders.

---

## **7. Key Interview Concepts Learned**

| Question                      | Short Answer                                                         |
| ----------------------------- | -------------------------------------------------------------------- |
| What is Wireshark used for?   | Capturing and analyzing network packets                              |
| What is a packet?             | Small unit of data transmitted across a network                      |
| Difference between TCP & UDP? | TCP is reliable & connection-oriented, UDP is fast & connection-less |
| What is a DNS query?          | Request made to obtain IP of a domain                                |
| Can Wireshark decrypt HTTPS?  | No, unless SSL keys are available                                    |
| How do filters help?          | They show only relevant packets/protocols                            |

---

## **8. Conclusion**

The Wireshark capture demonstrated real-time packet exchange between the system and remote servers.
Through protocol filtering, it became possible to clearly observe TCP handshakes, DNS lookups, encrypted HTTPS traffic, and ICMP communication.
This task improved understanding of network protocols and packet-level data flow, which is essential for network troubleshooting and cybersecurity analysis.

---
