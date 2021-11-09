# **Message Queues**

## **1. What are Message Queues ?**
A message queue is a component of messaging middleware solutions that enables independent applications and services to exchange information. Message queues store “messages”—packets of data that applications create for other applications to consume—in the order they are transmitted until the consuming application can process them. This enables messages to wait safely until the receiving application is ready, so if there is a problem with the network or receiving application, the messages in the message queue are not lost.

This model, known as asynchronous messaging, prevents data loss and enables systems to continue to function if processes or connections fail. This allows developers to keep processes and applications separate, keeping their communications self-contained and event-driven to make the architecture more reliable.

Message queues are available in messaging solutions across numerous deployment options, including optimized physical appliances, cloud services, mainframes, and as software.

![message Queue](https://miro.medium.com/max/886/0*0HsAVPt2ZCHl3gYl.jpg)

## **2. Types of Message Queues**

Actually, the system has different types of message queues: workstation message queue, user profile message queue, job message queue, system operator message queue, and history log message queue. Each of them have their own usage.
* Workstation message queues are used for sending and receiving messages between workstation users and between workstation users and the system operator. The name of the queue is the same as the name of the workstation. The queue is created by the system when the workstation is described to the system.

* User profile message queues can be used for communication between users. User profile message queues are automatically created in library QUSRSYS when the user profile is created.
* Job message queues are used for receiving requests to be processed (such as commands) and for sending messages that result from processing the requests; the messages are sent to the requester of the job. Job message queues exist for each job and only exist for the life of the job. Job message queues consist of an external message queue and a set of call stack entry message queues.
* System operator message queue is used for receiving and replying to messages from the system, display station users, and application programs.
* The history log message queue is used for any job in the system to have a record of high-level system activities.

In addition to these message queues, you can create your own user message queues for sending messages to system users and between application programs.


## **3. Why message queues are used ?**

Message queues are widely used across industries and can offer an array of benefits to developers and system administrators alike, including the following:

* **Reliable message delivery--** Using a message queue can ensure that business-critical messages between applications will not be lost and that they will be only be delivered to the recipient once. With this feature in place, additional de-duplication or loss-prevention logic is unnecessary.
* **Inter-application connectivity--** Some message queue solutions can handle message encryption, transactionality, and other communication aspects between applications and services. This simplifies application development and enables disparate architectures to work together.
* **Versatility--** Message queue solutions can support multiple languages, such as Java, Node.js, COBOL, C/C++, Go, .NET, Python, Ruby, and C#. They can also support numerous application programing interfaces (APIs) and protocols, including MQTT, AMQP, and REST, as well as others.
* **Resilience--** Asynchronous messaging ensures application-specific faults won’t impact the system. If one component in the system stalls, all others can continue interacting with the queue and processing messages. This decreases the chance that the entire system’s stability will be impacted by one part’s failure.
* **Improved security--** A message queue may be able to identify and authenticate all messages, and in some message queue solutions, they can be set to encrypt messages at rest, in transit, or end-to-end. This can contribute to the overall security of the applications and/or infrastructure.
* **Integrated file transfers--** Some message queue solutions include additional features, such as the ability to transfer files. This can be used as an alternative to FTP within enterprises where such solutions are in use.

## **4. Message Queue Tools**

Many message Queuing tools are out there in usage. Each of them have their own benefits. Some of widely using Message Queuing tools are:

- ### **Mulesoft Anypoint Platform**

    <img src="https://images.g2crowd.com/uploads/product/hd_favicon/1535025642/mulesoft-anypoint-platform.svg" alt="mulesoft" width="200"/>
    
    
    MuleSoft’s Anypoint Platform is a leading solution for API-led connectivity that creates an application network of apps, data, and devices, both on-premises and in the cloud. This hybrid integration platform includes iPaaS, ESB, and a unified solution for API management, design and publishing.
- ### **TIBCO Rendezvous**
   <img src="https://images.g2crowd.com/uploads/product/image/large_detail/large_detail_9091acdc0d44802da68c41c94f5ae5cc/tibco-rendezvous.jpg" alt="tibco" width="200"/>
   
   The TIBCO Enterprise Message Service standards-based Java Message Service (JSM) implementation allow any application that supports JMS, wheather home grow or third party, to quickly and easily exchange messages. Full TCK-certification with both the JMS 1.1 and 2.0 specification ensures compatiblity with other applications- as wel as a loosely coupled design for less overhead, time, and cost. As part of TIBCO Messaging, it supports seamless integration for hetrogeneous platforms, reduces system bottlenecks, increases scalability, and helps you respond faster to change.
- ### **VMWare Tanzu RabbitMQ**
   <img src="https://www.devopsschool.com/blog/wp-content/uploads/2021/07/image-30.png" alt="vmware" width="350"/>

   Messaging software serves as the central nervous system integrating distributed applications and services. Tanzu RabbitMQ makes it easy to architect resilient, loosely coupled systems. Application developers can connect systems using a variety of protocols and formats, without having to worry about interoperability, reliability, or scalability. Based on open source RabbitMQ, Tanzu RabbitMQ is lightweight and easy to deploy on premises and in the cloud. It’s a fast and dependable message broker that supports a wide range of use cases, including reliable integration, content-based routing and global data delivery, and high-volume monitoring and data ingestion.
   
- ### **Apache Kafka**
   <img src="https://images.g2crowd.com/uploads/product/image/large_detail/large_detail_809aa88d3571ee805a47d8fb156ba412/apache-kafka.jpg" alt="kaflka" width="200"/>
   
   Apache Kafka is an open-source distributed event streaming platform used by thousands of companies for high-performance data pipelines, streaming analytics, data integration, and mission-critical applications.
## **5. Enterprise Message Bus / Enterprise service bus (ESB)**  

An Enterprise Service Bus (ESB) is fundamentally an architecture. It is a set of rules and principles for integrating numerous applications together over a bus-like infrastructure. ESB products enable users to build this type of architecture, but vary in the way that they do it and the capabilities that they offer. 

<img src="https://miro.medium.com/max/700/1*jp1L2ShYDpDLHU8HCeVOhA.png" alt="ESB" width="600" height="400"/>

The core concept of the ESB architecture is that you integrate different applications by putting a communication bus between them and then enable each application to talk to the bus. This decouples systems from each other, allowing them to communicate without dependency on or knowledge of other systems on the bus. The concept of ESB was born out of the need to move away from point-to-point integration, which becomes brittle and hard to manage over time. Point-to-point integration results in custom integration code being spread among applications with no central way to monitor or troubleshoot. This is often referred to as "spaghetti code" and does not scale because it creates tight dependencies between applications.

There are some core functionalities that are under the hood of an ESB. These functions combine to make up the ESB architecture. They include :
* Decoupling
* Transport Protocol Conversion
* Message Enhancement
* Message Transformation

## **Reference**
[know more about messaging queues](https://www.ibm.com/cloud/learn/message-queues)

[Enterprise Service Bus](https://www.cleo.com/blog/knowledge-base-enterprise-service-bus-esb)










