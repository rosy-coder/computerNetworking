## 1. Basics of Computer Networking

### Basic Ideas

---

* **开放系统**(`Open system`)和**封闭系统**(`Closed system`)：*A system which is **connected to the network** and is **ready for communication.***

* **计算机网络**(`Computer NetWork`):多个设备(`devices`)（也称为主机(`hosts`)）的互连(`interconnection`)，这些设备使用多个路径进行连接，用于发送/接收数据或媒体(`data or media`)。计算机网络还可以包括多个设备/媒体(`devices/mediums`），有助于两种不同设备之间的通信：这些被称为**网络设备**（`Network devices`)，包括路由器(`routes`)、交换机(`switches`)、集线器(`hub`)和桥梁(`bridge`)等内容。

  ![computer network](https://media.geeksforgeeks.org/wp-content/uploads/Computer-Networking-Diagram.png)

* **网络拓扑**(`Network Topology`):

  网络中不同设备的布局安排(`layout arrangement`)。常见示例包括：总线(`bus`)、星形(`star`)、网状(`mesh`)、环形(`ring`)和雏菊链(`daisy chain`)。

  ![Network Topology](https://media.geeksforgeeks.org/wp-content/uploads/Network-Topology-Diagram.png)

* **OSI**:代表**开放系统互连**(`Open Systems Interconnection.`)。它是指定通信协议(`protocols`)标准以及每层功能的参考模型。

* **协议**(`Protocol`):协议是定义两个实体在网络中通信的方式的规则或算法集，OSI 模型的每一层都定义了不同的协议。比如 TCP、IP、UDP、ARP、DHCP、FTP 等。





### Unique Identifiers of Network

---

* **主机名称**(`Hostname`):Each device in the network is associated with a unique device name known as `Hostname`. 
  Type “hostname” in the command prompt(Administrator Mode) and press ‘Enter’, this displays the hostname of your machine. 

![hostname](https://media.geeksforgeeks.org/wp-content/uploads/hostname.png)

* **IP地址**(`(Internet Protocol address) `:Also known as the `Logical Address`, the IP Address is the ***network address of the system across the network.*** 
  为了识别全球网络中的每台设备，互联网分配号码管理局 （IANA） 为互联网上的每台设备分配了 IPV4 （版本 4） 地址作为唯一标识符。
  IPv4地址的长度是32位，因此，我们有2位32可用 IP 地址。IPv6 地址的长度为 128 位。
  *Type “ipconfig” in the command prompt and press ‘Enter’, this gives us the IP address of the device.*

* **MAC地址**(`Media Access Control address`):Also known as `physical address`, the MAC Address is the **unique identifier of each host** and is **associated with its NIC (Network Interface Card)**. 

  MAC 地址在制造时分配给 NIC.

  MAC 地址的长度为：12-nibble/ 6 字节/48。

  *Type “ipconfig/all” in the command prompt and press ‘Enter’, this gives us the MAC address.*

* **端口**(`port`):*A port can be referred to as a **logical channel** through which **data can be sent/received to an application**. Any host may have multiple applications running, and each of these applications is identified using the port number on which they are running.*

  *A port number is a **16-bit integer**, hence, we have 2^16 ports available which are categorized as shown below:*

  |         Port Types         |     Range     |
  | :------------------------: | :-----------: |
  |      Well known Ports      |   0 – 1023    |
  | Registered Ports(注册端口) | 1024 – 49151  |
  | Ephemeral Ports(临时端口)  | 49152 – 65535 |

  *Type “**netstat -a**” in the command prompt and press ‘Enter’, this lists all the ports being used.* 

* **Socket**:The unique combination of IP address and Port number together are termed as Socket. 



### Other related concepts

---

* **DNS服务器**(`DNS server`):DNS stands for **Domain Name system**(域名系统).

  DNS is basically a server which **translates web addresses or URLs (ex: www.google.com) into their corresponding IP addresses**. We don’t have to remember all the IP addresses of each and every website.

  ![dns](https://media.geeksforgeeks.org/wp-content/uploads/nslookup.png)

* **ARP**和**RARP**:

  * **ARP** stands for **Address Resolution Protocol**. 
    It is used to **convert an IP address to its corresponding physical address**(i.e., MAC Address). 
    ARP is used by the **Data Link Layer to identify the MAC address** of the Receiver’s machine.
  * **RARP** stands for **Reverse Address Resolution Protocol**. As the name suggests, it **provides the IP address of the device given a physical address as input.** But RARP has **become obsolete since the time DHCP has come into the picture.**



## 2. The Internet and the Web

About The difference between the Internet and the web,See[The Internet and the Web](https://www.geeksforgeeks.org/the-internet-and-the-web/)

| Internet                                                     | Web                                                          |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| The Internet is the network of networks and the network allows to exchange of the data between two or more computers. | The Web is a way to access Information through the Internet. |
| It is also known as Network of Networks.                     | The Web is a model for sharing information using Internet.   |
| The Internet is a way of transporting information between devices. | The protocol used by the web is Http.                        |
|                                                              | The Web is accessed by the Web Browser.                      |



## 3. Internet and Web programming

[This part](https://www.geeksforgeeks.org/internet-and-web-programming/) shows what will happen when we type  a URL like www.google.com.

![whole process](https://media.geeksforgeeks.org/wp-content/uploads/222-14.png)



## 4. Internet of Everything（`万物互联`）

[Here](https://www.geeksforgeeks.org/internet-of-everything/) introduces Internet of Everything(`IoE`) and its difference with Internet of Things(`物联网 IoT`).



## 5. Unknown facts of Networking

[Here](https://www.geeksforgeeks.org/unknown-facts-of-networking/) introduces several interesting facts about Networking.



## 6. Goals of Networks

See [Goals of Networks from geeksforgeeks.](https://www.geeksforgeeks.org/goals-of-networks/)

* **Networking Elements**:**–** The computer network includes the following networking elements: 
* **Network Criteria**:
  * **Performance –** It is measured in terms of `transit time` and `response time`.
  * **Reliability** 
  * **Security –** It means protecting data from unauthorized access. 
* **Goals of Computer Networks:** 
  * **Resource Sharing** 
  * **High Reliability**
  * **Inter-process Communication**
  * **Flexible access**



## 7. Line Configuration in Computer Networks

* `A network`is two or more devices connected through `a link`. 
*  `A link`is a communication pathway that transfer data from one device to another.

For communication to occur, two devices must be connected in some way to the same link at the same time. There are two possible types of connections:

1. **Point-to-Point Connection**
2. **Multipoint Connection**



### Point-to-Point Connection

1. 点对点连接提供两个设备之间的专用链接。
2. 链接的整个容量保留给这两个设备之间的传输。
3. 大多数点对点连接使用实际长度的电线或电缆连接两端，但其他选项，如微波或卫星链接也是可能的。
4. 点对点网络拓扑被认为是最简单和最传统的网络拓扑之一。
5. 这也是最简单的建立和理解。

![Point-to-Point](https://media.geeksforgeeks.org/wp-content/uploads/point-to-point-connection.jpg)



### Multipoint Connection

1. It is also called Multidrop configuration. In this connection two or more devices share a single link.
2. 超过两个设备共享的链接是通道的容量现在共享。在共享容量下，多点线配置中可能有两种可能性：
   * **空间共享：**如果多个设备可以同时共享链接，则其称为空间共享(`Spatial Sharing`)线路配置。
   * **时间共享：**如果用户必须轮流使用该链接，则其称为临时共享(`Temporally shared`)或时间共享(`Time Shared`)线路配置。



## 8. Transmission Modes in Computer Networks (Simplex, Half-Duplex and Full-Duplex)

![Transmission modes](https://media.geeksforgeeks.org/wp-content/uploads/transmissionmodes.png)

### (1) Simplex Mode

在Simplex Mode下，通信是单向的，就像在单向街道上一样。链接上的两个设备中只有一个可以传输，另一个只能接收。Simplex Mode可以使用通道的整个容量向一个方向发送数据。

示例：键盘和传统显示器。键盘只能引入输入，显示器只能给输出。

![Simplex one direction](https://media.geeksforgeeks.org/wp-content/uploads/SiMpleduplex.png)

### (2) **Half-Duplex Mode** (半双工)

在半双工模式下，每个站可以同时传输和接收，但不能同时传输和接收。当一个设备发送时，另一个设备只能接收，反之亦然。半双工模式用于同时不需要双向通信的情况下。通道的整个容量可用于每个方向。
示例：对讲机，其中消息一次发送一个，消息以两个方向发送。

![Half-Duplex](https://media.geeksforgeeks.org/wp-content/uploads/halfduplex.png)

```text
Channel capacity=Bandwidth * Propagation Delay
```



### (3)  **Full-Duplex Mode**(全双工)

在全双工模式下，两个站可以同时传输和接收。在全双工模式下，朝一个方向移动的信号与指向其他方向的信号共享链接的容量，这种共享可以通过两种方式发生：

- 该链接必须包含两个物理独立的传输路径，一个用于发送，另一个用于接收。
- 或者容量在双向移动的信号之间分配。

```text
Channel Capacity=2* Bandwidth*propagation Delay
```

![Full-Duplex](https://media.geeksforgeeks.org/wp-content/uploads/fullduplex.png)



## 9. Types of Transmission Media

1. **Guided Media:** 

   **(i) Twisted Pair Cable**

   * **Unshielded Twisted Pair (UTP):**
   * **Shielded Twisted Pair (STP):** 

   **(ii) Coaxial Cable**

   **(iii) Optical Fibre Cable** 

   **(iv) Stripline**

   **(v) Microstripline**



2. **Unguided Media:** 

   **(i) Radiowaves**

   **(ii) Microwaves**

   **(iii) Infrared**(红外波)



See More in [this passage](https://www.geeksforgeeks.org/types-transmission-media/).



## 10. Difference between Unicast, Broadcast and Multicast in Computer Network

* **Unicast**

  ![uc](https://media.geeksforgeeks.org/wp-content/uploads/UNICAST-1.png)

* **Broadcast**

  * **Limited Broadcast**(255.255.255.255)

    ![Lb](https://media.geeksforgeeks.org/wp-content/uploads/NETWORK-CLUSTER.png)

  * **Direct Broadcast**(This is achieved by translating **all the Host ID part bits of the destination address to 1**)

    ![db](https://media.geeksforgeeks.org/wp-content/uploads/DIRECT_BROADAST.png)

* **Multicast**





## 11. Introduction to basic Networking terminology

* **Network**:*For a specific purpose if things are connected together, are referred as a **NETWORK**. A network can be of many types, like a telephone network, television network, computer network or even a people network.*

* **COMPUTER NETWORK** : *a **COMPUTER NETWORK** is also a kind of setup, where it connects two or more devices to share a range of services and information in the form of **e-mails and messages**, **databases**, **documents**, **web-sites**, **audios and videoes**, **Telephone calls and video conferences** etc among them.*

*  **PROTOCOL**:*A **PROTOCOL** is nothing but set of defined **rules**, which has to be followed by every connected devices across a network to communicate and share information among them. To facilitates **End to End** communication, a number of protocols worked together to form a **Protocol Suites or Stacks**.*

  **Some basic Protocol**

  * **IP** : Internet Protocol
  * **FTP** : File Transfer Protocol
  * **SMTP** : Simple Mail Transfer Protocol
  * **HTTP** : Hyper Text Transfer Protocol

* **Network reference models** :A network reference model serves as a blueprint, detailing standards for how protocol communication should occur.

  **Two reference models**:

  * the **Open Systems Interconnect** ( **[OSI](https://www.geeksforgeeks.org/layers-osi-model/)** ) Model 
  * **Department of Defense** ( DoD, also known as **[TCP/IP](https://www.geeksforgeeks.org/computer-network-tcpip-model/)** ) model

* **Network Types**:

  According to the `size`, the network can be commonly categorized into **Three **types.

  * **LANs (Local Area Networks)**
  * **MANs (Metropolitan Area Networks)**
  * **WANs (Wide Area Networks)**

  

  categorized by their `function`.

  * **[SAN ](https://www.geeksforgeeks.org/storage-area-networks/)(Storage Area Network)：**A SAN provides systems with high-speed, lossless access to high-capacity storage devices.
  * **[VPN](https://www.geeksforgeeks.org/virtual-private-network-vpn-introduction/) (Virtual Private Network)**: A VPN allows for information to be securely sent across a public or unsecure network, such as the Internet. Common uses of a VPN are to connect branch offices or remote users to a main office.

* **Host**:In a network, any connected device is called as **host**

  - A host can acts as a ***Client\***, when he is requesting information.
  - A host can acts as a ***Server\***, when he provides information.
  - A host can also request and provide information, is called ***Peer\***.



## 12. Types of Network Topology

[This passage](https://www.geeksforgeeks.org/types-of-network-topology/) discusses different types of Network Topology and their advantages and disadvantages.



## 13. [Types of area networks – LAN, MAN and WAN](https://www.geeksforgeeks.org/types-of-area-networks-lan-man-and-wan/)



## 14. Telecom Networks

[Hard to understand](Telecom Networks).

Discuss some concepts about telecom networks



## 15.Access Networks

An **access network** is a type of network which physically connects an end system to the immediate router (also known as the “edge router”) on a path from the end system to any other distant end system.

**Types of access networks:**

* **Ethernet**
* **DSL** --`Digital Subscriber Line`
* **FTTH**--`Fiber to the home`
* **Wireless LANs**
* **3G and LTE**



## 16. TCP/IP Model

The **OSI Model** we just looked at is just a reference/logical model. It was designed to describe the functions of the communication system by dividing the communication procedure into smaller and simpler components. 

The **TCP/IP model** is a concise version of the OSI model. It contains four layers, unlike seven layers in the OSI model. The layers are:

1. Process/Application Layer
2. Host-to-Host/Transport Layer
3. Internet Layer
4. Network Access/Link Layer

![difference between TCP/IP and OSI](https://media.geeksforgeeks.org/wp-content/uploads/tcpAndOSI.png)

* ###  Network Access Layer 

  This layer corresponds to the **combination of Data Link Layer and Physical Layer **of the OSI model. It looks out for hardware addressing and the protocols present in this layer allows for the physical transmission of data.

  `ARP `is a protocol of Internet layer, but there is a conflict about declaring it as a protocol of Internet Layer or Network access layer. It is described as residing in layer 3, being encapsulated by layer 2 protocols.

* ###  Internet Layer

  This layer parallels the functions of OSI’s **Network layer**. It defines the protocols which are responsible for logical transmission of data over the entire network.

  * **IP** **–** stands for Internet Protocol .
  * **ICMP**-Internet Control Message Protocol. It is encapsulated within IP datagrams and is responsible for providing hosts with information about network problems.
  * **ARP** -stands for Address Resolution Protocol.ARP has several types: Reverse ARP, Proxy ARP, Gratuitous ARP and Inverse ARP.

* ### Host-to-Host Layer

  This layer is analogous to the **transport layer** of the OSI model. It is responsible for **end-to-end communication** and **error-free delivery of data.** It shields the upper-layer applications from the complexities of data. The two main protocols present in this layer are :

  * **Transmission Control Protocol (TCP)**
  * **User Datagram Protocol (UDP)** 

* ### Application Layer 

  This layer performs the functions of top three layers of the OSI model: **Application, Presentation and Session Layer.**

   [Protocols in Application Layer](https://www.geeksforgeeks.org/protocols-application-layer/) And three:

  * **HTTP and HTTPS**-Hypertext transfer protocol (secure)
  * **SSH**-Secure Shell
  * **NTP** -Network Time Protocol



## 17. Layers of OSI Model

 

