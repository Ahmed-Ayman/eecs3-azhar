TOC 
-----
* [question 1](https://github.com/Ahmed-Ayman/eecs3-azhar/blob/master/sheet2.md#q1)
* [question 8](https://github.com/Ahmed-Ayman/eecs3-azhar/blob/master/sheet2.md#q8)
* [question 9](https://github.com/Ahmed-Ayman/eecs3-azhar/blob/master/sheet2.md#q9)

<a href = 'q1'></a>
# Question 1
Explain with the required figures (Data Rate, Channel Capacity, Bandwidth Of Channel, Nyquist Bit Rate)
- **Data Rate:**
  Transmission rate, also known as data rate, is the number of bits transmitted during
  a period of time divided by that time and is measured in bits per second (bps).

- **Channel Capacity:**
  The maximum rate at which data can be transmitted over a
  communication channel under given conditions is referred as the channel capacity.

- **Bandwidth Of Channel:**
  Bandwidth merely specifies a range of frequencies, from the lowest to
  the highest, that the channel can carry or that are present in the signal. It
  is one way of describing the maximum amount of information that the
  channel can carry. Bandwidth is expressed differently for analog and
  digital circuits. In analog technology, the bandwidth of a circuit is the
  difference between the lowest and highest frequencies that can pass
  through the channel. Engineers measure analog bandwidth in kilohertz or megahertz.

 - **Nyquist Bit Rate:**
  The Nyquist bit rate formula defines the theoretical maximum bit rate for a noiseless channel *(Bitrate = 2 x Bandwidth x Log2 L)*
    - Where,
      - Bitrate is the bitrate of the channel in bits per second.
      - Bandwidth is the bandwidth of the channel.
      - L is the number of signal levels.


 - **Shannon Channel Capacity:**
  The Shannon Capacity defines the theoretical maximum bit rate for a noisy channel *(Capacity = bandwidth x log2(1 + SNR))*
    - Where,
      - Capacity is the capacity of the channel in bits per second.
      - Bandwidth is the bandwidth of the channel.
      - SNR is the Signal to Noise Ratio.
------
<a href = 'q8'></a>

# Question 8

### Explain in specific points the important functions (jobs) of the following layers:

* Application Layer.
* Presentation Layer.
* Session Layer.
* Transport Layer.
* Network Layer.
* Data link layer.
-------------
# Answer

1) **Application Layer** :
>serves the user and performs all kind of requests such as sharing files, printing files,e-mails, it uses Protocol Data Unit (PDU) to  build a form for a message from the source to the destination.

 PDU format:


 |  ID of S | Date (dd/mm/yy) |
 |----------|-----------------|

2) **Presentation Layer**
>this layer allows us to see the recieved data in the correct format , like the letters,pictures,videos just like the way the sent.
so, it defines how data in the native format of the remote host should be presented in the native format of host.


 PDU format:

 |  ID of S | Date (mm/dd/yy) |
 |----------|-----------------|

3) **Session Layer**

> uts designed to perform inter-node communication. its  establishes,manages,and terminates sessions between applications.
so its maintains sessions between remote hosts. For example, once user/password authentication is done, the remote host maintains this session for a while and does not ask for authentication again in that time span.


 PDU format:

 |  ID of S | Date (mm/dd/yy) |length|
 |----------|-----------------|------|


4) **Transport Layer**
> This layer is concerned with the transportation of the messages from the source to the destination in correct formats and correct sequence, it uses flow control techniques.
so, its responsible for end-to-end delivery between hosts.

PDU format:

|  ID of S | Date (mm/dd/yy) |length|checksum|
|----------|-----------------|------|--------|

 5) **Network Layer**
 >
 This layer constructs a routing table to choose the best route from Source to destination that across a number of transmission links and network nodes to reach the destination
 so, its responsible for address assignment and uniquely addressing hosts in a network.
 PDU format:

 |  ID of S | destination address|date|length|packet sequence|checksum error|
 |----------|--------------------|----|------|---------------|---------|


 PDU format:

 |  Header  | Data |Tailer|
 |----------|-----------------|------|

 6) **Data link Layer**
 >This layer is concerned with Transmitting the data from the source to the destination nodes, it appends Header and trailer to message to construct a frame that is proportional to the type of protocol that is used in the network.
 so, its responsible for handling the reading and the writing of the data and the Link errors are detected at this layer.

Optional!!

 7) **Physical Layer**
 This layer defines the hardware, cabling wiring, power output, pulse rate etc.

 ----------------
<a href = 'q9'></a>

# Question 9

#### what is the difference between (Data link layer, Network layer, Transport layer) from the point of sending a message from source to destination nodes and  their functions ?

#### Data link layer

>The data link layer provides node-to-node data transfer—a link between two directly connected nodes. It detects and possibly corrects errors that may occur in the physical layer. It defines the protocol to establish and terminate a connection between two physically connected devices. It also defines the protocol for flow control between them.

#### Network layer
>The network layer provides the functional and procedural means of transferring variable length data sequences (called datagrams) from one node to another connected in "different networks".

#### Transport layer
>The transport layer provides the functional and procedural means of transferring variable-length data sequences from a source to a destination host via one or more networks, while maintaining the quality of service functions.
