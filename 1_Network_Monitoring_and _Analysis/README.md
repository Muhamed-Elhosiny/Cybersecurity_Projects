
# Network Traffic Analysis Using Tcpdump and Wireshark

## Objective
This project demonstrates my ability to capture and analyze network traffic using `tcpdump` for packet capture and Wireshark for detailed analysis.

## Workflow

### 1. Capture with Tcpdump
- **Command:**
 
![image](https://github.com/user-attachments/assets/8352de0f-7b4b-4c62-8d99-86a3db0f1e2b)


Captured all packets on the eth0 interface and saved them to capture.pcap.

## 1. Install Wireshark on Linux 

![image](https://github.com/user-attachments/assets/806af965-bfeb-4a91-8edf-766878005fae)


## 2. Analyze with Wireshark

I Navigated to where the capture.pcap and start to analyze it with wireshark

![image](https://github.com/user-attachments/assets/c6c41527-0eda-45bc-acf4-b73a8f91a90b)


## Analysis of Packet Details

## Packet Content:

## Ethernet Header: 
The initial bytes 00 15 5d 6f 6c 67 00 15 5d c9 e5 15 represent the source and destination MAC addresses, which are used for communication within a local network.

## IP Header: 

Following the Ethernet header, 08 00 indicates that the payload is an IPv4 packet. The IP header includes source and destination IP addresses and various flags and options related to packet routing and handling.

## Payload: 
The payload section (e.g., 45 00 00 54 1e 82 40 00 40 01 35 f5) shows the start of the IP header and encapsulated data. The observed payload also contains the ICMP echo request and response (from ping), which include the sequence number and payload data.


## Obsevation

## Traffic Patterns: 
The capture includes a series of packets in response to the ICMP echo request, indicating successful communication with google.com. Each ICMP echo request and reply is visible, reflecting round-trip times and packet size.

## Anomalies: 
In this particular capture, no significant anomalies were observed. All packets appear to be consistent with normal ICMP traffic. However, in different scenarios, anomalies such as packet loss, high latency, or malformed packets could be identified using similar techniques.

## Conclusion
This project showcases my proficiency in using tcpdump for network traffic capture and Wireshark for detailed traffic analysis. The ability to troubleshoot and analyze network issues is crucial for maintaining secure and efficient systems.
