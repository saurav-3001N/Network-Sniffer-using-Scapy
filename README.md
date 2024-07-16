# Network Packet Sniffer

This is a Python-based network packet sniffer that captures and logs network packets on a specified interface. It allows filtering by protocol and logs packet information to a file.

## Features

- Captures packets on a specified network interface
- Can filter packets by protocol (ARP, BOOTP, ICMP, or all protocols)
- Logs packet information (timestamp, protocol, source MAC, and destination MAC) to a file
- Configures the network interface to promiscuous mode for packet capturing

## Prerequisites

- Python 3.x
- Scapy library

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/saurav-3001N/network-packet-sniffer.git
    cd network-packet-sniffer
    ```

2. Install the required dependencies:

    ```sh
    pip install -r requirements.txt
    ```

    If `requirements.txt` doesn't exist, install Scapy manually:

    ```sh
    pip install scapy
    ```

## Usage

1. Run the program with root privileges:

    ```sh
    sudo python packetSniffer.py
    ```

2. Follow the prompts to enter the required parameters:
    - Interface on which to run the sniffer (e.g., `enp0s8`)
    - Number of packets to capture (0 for infinity)
    - Time interval to run the capture (in seconds)
    - Protocol to filter by (`arp`, `bootp`, `icmp`, or `0` for all protocols)
    - Name of the log file to save captured packets

3. The program will start capturing packets based on your inputs and log them to the specified file.

## Example

Here is an example of running the sniffer:

```sh
! Make sure to run this program as ROOT !

* Enter the interface on which to run the sniffer (e.g. 'enp0s8'): enp0s8

Interface enp0s8 was set to PROMISC mode.

* Enter the number of packets to capture (0 is infinity): 10

The program will capture 10 packets.

* Enter the number of seconds to run the capture: 60

The program will capture packets for 60 seconds.

* Enter the protocol to filter by (arp|bootp|icmp|0 is all): icmp

The program will capture only ICMP packets.

* Please give a name to the log file: capture_log.txt

* Starting the capture...

* Please check the capture_log.txt file to see the captured packets.



```sh
For a video tutorial, visit [this link](https://www.linkedin.com/posts/saurav-s-0685a7234_security-awareness-activity-7153086124247142401-_7QO?utm_source=share&utm_medium=member_desktop).



