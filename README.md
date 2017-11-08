## Table Of Contents

* [What is OSI model?](#what-is-open-systems-interconnection-model)
* [7 layers computer network](#7-open-systems-interconnection-layers)
* [OSI vs TCP/IP(Transmission Control Protocol / Internet Protocol)](#osi-vs-tcp/ip)
* [Credits and resources](#credits-and-resources)

### What is open systems interconnection model?

* OSI (Open Systems Interconnection) is reference model for how applications can communicate over network.
* The purpose of the OSI reference model is to guide vendors and developers so the digital communication products and software programs they create will interoperate, and to facilitate clear comparisons among communications tools.
* The main concept of OSI is that the process of communication between two endpoints in a telecommunication network can be divided into seven distinct groups of related functions, or layers.
* The sever layers of function are provided by a communication of applications, operating systems, network card device drivers and networking hardware that enable a system to put a signal on a network cable or out over Wi-Fi or other wireless protocol.

### 7 open systems interconnection layers

<p align="center">
  <img src="https://luiscachog.me/wp-content/uploads/2017/09/OSI-TCP-Model-v1.png">
</p>

* [Layer 7 - Application layer](#application-layer)
* [Layer 6 - Presentation layer](#presentation-layer)
* [Layer 5 - Session layer](#session-layer)
* [Layer 4 - Transport layer](#transport-layer)
* [Layer 3 - Network layer](#network-layer)
* [Layer 2 - Data link layer](#data-link-layer)
* [Layer 1 - Physical layer](#physical-layer)

### Application layer

* The application layer is the interface between the protocol stack and application software.
* The software might be client utilities or server services.
* The application layer is assigned the responsibility to check whether a remote communication partner is available, confirm communications with that partner are possible, and evaluate whether or not there are sufficient resources to maintain a communication.
* It is important to know that software, like a Web browser Chrome or Skype or an e-mail service, is not part of the application server; rather, they communicate with protocols in the application layer.
* Most applications have a specific protocol designed around their data types, functions, and features.
* Most commonly used application protocols are:
  * **HTTP** - hypertext transfer protocol
  * **FTP** - file transfer protocol
  * **SMTP** - simple mail transfer protocol
  * **POP3** - post office protocol
  * **IMAP** - internet message access protocol
  * **DNS** - domain name service
  * **Telnet**
* Commonly application layer functions are:
  * **Network Virtual Terminal**
  * **FTAM** - File transfer access and management
  * **Mail Services**
  * **Directory Services**
  * **Remote printer access**
  * **Network management**
  * **Resource sharing and device redirection**
  * **Remote file access**

### Presentation layer

* Presentation layer is also called the **Translation layer**.
* The data from the application layer is extracted here and manipulated as per the required format to transmit over the network.
* This layer may translate data from a format used by the application layer into a common format at the sending end, then translate the common format to a format known to the application layer at the receiving end.
* The presentation layer functions are:
  * **Character code translation**: for example, ASCII to EBCDIC.
  * **Data conversion**: bit order, CR-CR/LF, integer-floating point, and so on.
  * **Data compression**: reduces the number of bits that need to be transmitted on the network.
  * **Data encryption**: encrypt data for security purposes. For example, password encryption.

### Session layer

* Session layer manages the connections between computers.
* Session layer functions are:
  * **Session establishment, maintenance and termination**: allows two application processes on different machines to establish, use and terminate a connection, called a session.
  * **Session support**: performs the functions that allow these processes to communicate over the network, performing security, name recognition, logging, and so on.

### Transport layer

* Transport layer ensures that messages are delivered error-free, in sequence, and with no losses or duplications.
* Transport layer is called as **Heart of OSI** model.
* The size and complexity of a transport protocol depends on the type of service it can get from the network layer.
* The transport layer functions are:
  * **Message segmentation**: accepts a message from the (session) layer above it, splits the message into smaller units (if not already small enough), and passes the smaller units down to the network layer. The transport layer at the destination station reassembles the message.
  * **Message acknowledgment**: provides reliable end-to-end message delivery with acknowledgments.
  * **Message traffic control**: tells the transmitting station to "back-off" when no message buffers are available.
  * **Session multiplexing**: multiplexes several message streams, or sessions onto one logical link and keeps track of which messages belong to which sessions (see [session layer](#session-layer)).

### Network layer

* Network layer works for the transmission of data from one host to the other located in different network.
* It also takes care of packing routing i.e. selection of shortest path to transmit the packet, from the number of routes available.
* The sender & receiver's IP address are placed in the header by network layer.
* The network layer functions are:
  * **Routing**: routes frames among networks.
  * **Subnet traffic control**: routers (network layer intermediate systems) can instruct a sending station to "throttle back" its frame transmission when the router's buffer fills up.
  * **Frame fragmentation**: if it determines that a downstream router's maximum transmission unit (MTU) size is less than the frame size, a router can fragment a frame for transmission and re-assembly at the destination station.
  * **Logical-physical address mapping**: translates logical addresses, or names, into physical addresses.
  * **Subnet usage accounting**: has accounting functions to keep track of frames forwarded by subnet intermediate systems, to produce billing information.

### Data link layer

* Data link layer is responsible for the node to node delivery of message.
* The main function of this layer is to make sure data transfer is error free from one node to another, over the physical layer.
* When a packet arrives in a network, it is the responsibility of DLL to transmit it to the Host using its MAC address.
* The data link layer functions are:
  * **Link establishment and termination**: establishes and terminates the logical link between two nodes.
  * **Frame traffic control**: tells the transmitting node to "back-off" when no frame buffers are available.
  * **Frame sequencing**: transmits/receives frames sequentially.
  * **Frame acknowledgment**: provides/expects frame acknowledgments. Detects and recovers from errors that occur in the physical layer by retransmitting non-acknowledged frames and handling duplicate frame receipt.
  * **Frame delimiting**: creates and recognizes frame boundaries.
  * **Frame error checking**: checks received frames for integrity.
  * **Media access management**: determines when the node "has the right" to use the physical medium.

### Physical layer

* The lowest layer of the OSI reference model is the physical layer.
* The physical layer contains information in the form of **bits**.
* It describes the electrical/optical, mechanical, and functional interfaces to the physical medium, and carries the signals for all of the higher layers.
* When receiving data, this layer will get the signal received and convert it into 0s and 1s and send them to the Data Link layer, which will put the frame back together.
* The physical layer functions are:
  * **Data encoding**: modifies the simple digital signal pattern (1s and 0s) used by the PC to better accommodate the characteristics of the physical medium, and to aid in bit and frame synchronization. It determines:
    * What signal state represents a binary 1
    * How the receiving station knows when a "bit-time" starts
    * How the receiving station delimits a frame
  * **Bit synchronization**: The physical layer provides the synchronization of the bits by providing a clock. This clock controls both sender and receiver thus providing synchronization at bit level.
  * **Bit rate control**: The Physical layer also defines the transmission rate i.e. the number of bits sent per second.
  * **Physical topologies**: Physical layer specifies the way in which the different, devices/nodes are arranged in a network i.e. bus, star or mesh topolgy.
  * **Transmission mode**: Physical layer also defines the way in which the data flows between the two connected devices. The various transmission modes possible are: Simplex, half-duplex and full-duplex.

### OSI vs TCP/IP

<p align="center">
  <img src="https://computergardens.files.wordpress.com/2015/09/osi-tcp-model.gif?w=400&h=311">
</p>

<table>
<tbody><tr><th>OSI(Open System Interconnection)</th><th>TCP/IP(Transmission Control Protocol / Internet Protocol)
</th></tr>
<tr><td>1. OSI is a generic, protocol independent standard, acting as a communication gateway between the network and end user.</td><td>1. TCP/IP model is based on standard protocols around which the Internet has developed. It is a communication protocol, which allows connection of hosts over a network.</td></tr>
<tr><td>2. In OSI model the transport layer guarantees the delivery of packets.</td><td>2. In TCP/IP model the transport layer does not guarantees delivery of packets. Still the TCP/IP model is more reliable.</td></tr>
<tr><td>3. Follows vertical approach.</td><td>3. Follows horizontal approach.</td></tr>
<tr><td>4. OSI model has a separate Presentation layer and Session layer.</td><td>4. TCP/IP does not have a separate Presentation layer or Session layer.</td></tr>
<tr><td>5. OSI is a reference model around which the networks are built. Generally it is used as a guidance tool.</td><td>5. TCP/IP model is, in a way implementation of the OSI model.</td></tr>
<tr><td>6. Network layer of OSI model provides both connection oriented and connectionless service. </td><td>6. The Network layer in TCP/IP model provides connectionless service.</td></tr>
<tr><td>7. OSI model has a problem of fitting the protocols into the model.</td><td>7. TCP/IP model does not fit any protocol</td></tr>
<tr><td>8. Protocols are hidden in OSI model and are easily replaced as the technology changes. </td><td>8. In TCP/IP replacing protocol is not easy.</td></tr>
<tr><td>9. OSI model defines services, interfaces and protocols very clearly and makes clear distinction between them. It is protocol independent.</td><td>9. In TCP/IP, services, interfaces and protocols are not clearly separated. It is also protocol dependent.</td></tr>
<tr><td>10. It has 7 layers</td><td>10. It has 4 layers</td></tr>
</tbody>
</table>
