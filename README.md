# Internet Routing — Advanced Computer Networks

A computer networking project for the **Advanced Computer Networks (AdCN)** course, focusing on **Internet Routing** and network configuration using **GNS3**.

The project provides a virtual network topology that can be imported into GNS3 for studying and experimenting with routing behavior between different network segments.

## 📌 Project Overview

This project simulates an Internet routing environment using **GNS3**. The topology consists of multiple routers and network segments that communicate through configured routing protocols.

The main objectives are:

* Build and configure a virtual Internet-like network topology.
* Configure routing between different networks.
* Observe routing tables and packet forwarding.
* Analyze how packets travel through the network.
* Verify connectivity between different network segments.
* Practice troubleshooting routing and connectivity problems.

## 🛠️ Technologies

| Technology                    | Purpose                                      |
| ----------------------------- | -------------------------------------------- |
| [GNS3](https://www.gns3.com/) | Network topology simulation                  |
| Cisco IOS / Router images     | Router configuration and routing             |
| IPv4                          | Network addressing and packet forwarding     |
| Routing Protocols             | Exchange routing information between routers |

## 📂 Repository Structure

```text
adcn-internet-routing/
│
├── 23120074_23120094.gns3project
│   ├── project-files/
│   ├── README.txt
│   └── project.gns3
│
├── 23120074_23120094.gns3project.zip
│
├── Report.pdf
│
├── README.md
│
└── README.txt
```

### Main Files

**`23120074_23120094.gns3project`**

The main GNS3 project containing the network topology and project configuration.

**`23120074_23120094.gns3project.zip`**

Compressed version of the GNS3 project for convenient distribution or import.

**`Report.pdf`**

The project report containing the network design, configuration, experiments, and analysis.

## 🚀 Getting Started

### 1. Prerequisites

Install the following software before running the project:

* [GNS3](https://www.gns3.com/)
* Required router appliance / IOS images compatible with the project
* A supported virtualization environment if required by the selected GNS3 setup

Make sure the required router images are available in GNS3 before opening the project.

### 2. Clone the Repository

```bash
git clone https://github.com/nvphuoc1172/adcn-internet-routing.git
cd adcn-internet-routing
```

### 3. Import the GNS3 Project

Open **GNS3** and import the project:

```text
File
  → Import portable project
  → Select 23120074_23120094.gns3project
```

Alternatively, extract:

```text
23120074_23120094.gns3project.zip
```

and import the resulting GNS3 project.

> **Note:** Depending on the GNS3 version and local configuration, some router appliances or IOS images may need to be mapped manually after importing the project.

### 4. Start the Topology

After importing the project:

1. Open the project in GNS3.
2. Check that all required router nodes are available.
3. Start the required nodes.
4. Wait until the routers finish booting.
5. Verify the network interfaces and IP addresses.
6. Enable or verify the configured routing protocols.
7. Check the routing tables.
8. Test connectivity between network segments.

For a quick test, use commands such as:

```text
ping <destination-ip>
traceroute <destination-ip>
```

On Cisco routers, useful commands include:

```text
show ip interface brief
show ip route
show running-config
```

Routing-protocol-specific commands can also be used to inspect neighbor relationships and learned routes.

## 🌐 Network Topology

The project uses GNS3 to emulate an interconnected router topology representing an Internet routing environment.

A simplified representation is:

```text
                 ┌─────────────┐
                 │   Network   │
                 │   Segment A │
                 └──────┬──────┘
                        │
                   ┌────▼────┐
                   │ Router  │
                   │    R1   │
                   └────┬────┘
                        │
              ┌─────────┴─────────┐
              │                   │
         ┌────▼────┐         ┌────▼────┐
         │ Router  │         │ Router  │
         │    R2   │─────────│    R3   │
         └────┬────┘         └────┬────┘
              │                   │
         ┌────▼────┐         ┌────▼────┐
         │ Network │         │ Network │
         │ Segment │         │ Segment │
         │    B    │         │    C    │
         └─────────┘         └─────────┘
```

> The actual topology is available directly in the GNS3 project file.

## 🔍 Experiments

The project can be used to perform experiments such as:

### Routing Table Verification

Inspect the routing table on each router:

```text
show ip route
```

This allows us to determine which networks are directly connected and which routes have been learned dynamically.

### Connectivity Testing

Use `ping` to verify end-to-end connectivity:

```text
ping <destination-ip>
```

### Path Analysis

Use `traceroute` to determine the path taken by packets:

```text
traceroute <destination-ip>
```

This is useful for observing how packets are forwarded through intermediate routers.

### Routing Protocol Analysis

The routing configuration can be inspected to understand:

* Neighbor relationships
* Route advertisement
* Route learning
* Route selection
* Routing table updates
* Packet forwarding behavior

## 🧪 Verification

After starting the topology, the following checks should be performed:

* [ ] All required routers are running.
* [ ] Router interfaces are configured correctly.
* [ ] Interfaces are in the `up/up` state.
* [ ] IP addressing is correct.
* [ ] Routing neighbors are established where required.
* [ ] Expected routes appear in the routing tables.
* [ ] End-to-end `ping` succeeds.
* [ ] `traceroute` follows the expected path.

Example:

```text
Router# show ip interface brief
Router# show ip route
Router# ping <destination-ip>
Router# traceroute <destination-ip>
```

## 📑 Project Report

The complete project report is available in:

```text
Report.pdf
```

The report provides additional details about the network topology, configuration, experiments, and analysis.

## 👥 Authors

This project was developed for the **Advanced Computer Networks** course by:

| Name                 | Student ID |
| -------------------- | ---------- |
| **Nguyễn Văn Phước** | 23120074   |
| **Hà Công Thuận**    | 23120094   |

## 📚 Course

**Advanced Computer Networks (AdCN)**

### Topic

**Internet Routing**

### Tools

**GNS3**

## ⚠️ Notes

The project depends on the router appliances / IOS images configured in the original GNS3 environment.

If the project does not start correctly after importing, check:

1. Whether the required GNS3 appliances are installed.
2. Whether the corresponding router images are available.
3. Whether the appliance names match the original project.
4. Whether the network interfaces are mapped correctly.
5. Whether the GNS3 version is compatible with the project.

The GNS3 project contains the actual network configuration and topology; the repository itself does not provide proprietary Cisco IOS images.

## 🔗 Repository

[GitHub — adcn-internet-routing](https://github.com/nvphuoc1172/adcn-internet-routing)
