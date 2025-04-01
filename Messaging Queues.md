# Messaging Queues

A message queue is a form of asynchronous service-to-service communication used in serverless and microservices architectures. Messages are stored on the queue until they are processed and deleted. Each message is processed only once, by a single consumer.

Message queues can be used to decouple heavyweight processing, to buffer or batch work, and to smooth spiky workloads.

Message queues allow different parts of a system to communicate and process operations asynchronously. A message queue provides a lightweight buffer which temporarily stores messages, and endpoints that allow software components to connect to the queue in order to send and receive messages.

The messages are usually small, and can be things like requests, replies, error messages, or just plain information. To send a message, a component called a producer adds a message to the queue. The message is stored on the queue until another component called a consumer retrieves the message and does something with it.

![message queues](https://d1.awsstatic.com/product-marketing/Messaging/sqs_seo_queue.1dc710b63346bef869ee34b8a9a76abc014fbfc9.png)

## What are Messaging Queues?

1. A message queue is a form of middleware used in software development to enable communications between services, programs, and dissimilar components, such as operating systems and communication protocols.
2. A message queue enables the smooth flow of information to make complex systems work.
3. The concept is like text messaging—a feature most mobile phone users understand. If you need to send a message, you can call someone. However, that assumes they are available and have time to talk.
4. For non-urgent messages, texting is a more efficient approach. The message goes into a queue on the recipient’s phone, and they respond when possible.
5. In a distributed processing environment, message queuing is similar, although the speed and volume of messages are much greater.
6. Queued messages are typically small and specific. They may be requests, replies, error messages, or information needed for logging or tracing. A producer creates the message, and a consumer processes it.
   <br>

### Advanced Message Queuing Protocol

1. The Advanced Message Queuing Protocol (AMQP) is an open standard for passing messages between applications and organizations.

2. It provides a consistent platform that integrates with a variety of message queuing types to enable consistent performance regardless of the platform.
3. **Reliable message delivery**: Using a message queue can ensure that business-critical messages between applications will not be lost and that they will only be delivered to the recipient once. With this feature in place, additional de-duplication or loss-prevention logic is unnecessary.
4. **Inter-application connectivity**: Some message queue solutions can handle message encryption, transactionality and other communication aspects between applications and services. This simplifies application development and enables disparate architectures to work together.
5. Improved security: A message queue may be able to identify and authenticate all messages. In some message queue solutions, they can be set to encrypt messages at rest, in transit or end-to-end. This can contribute to the overall security of the applications and infrastructure.
6. **Scalability**: Message queues can be designed to scale with the needs of their applications. This means that they can handle a large volume of messages and can be easily expanded to meet the needs of the business.

## Why they are used?

1. Today’s enterprise computing environments are complex and highly decentralized. Messaging makes it easier to integrate applications and services on diverse platforms by providing a single, robust and secure shared messaging backbone. This protects against data loss and ensures that systems continue to function even with unstable connectivity.
2. Message queues are uniquely suited for integrating on-premises backend systems with cloud services. In cloud architectures, applications are often broken down into small, independent components.
3. This makes it easier to design and code them, and also easier to manage their performance. Message queues enable these decoupled cloud-based applications to communicate with each other or with on-premises systems.
4. Message queuing increases architecture resilience because the messages can have persistence. This means they’re stored to disk until the service receiving the message confirms processing.
5. Messaging queues can be used in scenarios requiring high levels of security, fault tolerance and accuracy, such as financial transaction processing, air-travel booking or updating healthcare patient records.
6. Message queues can also be used to enable applications and systems residing in different clouds (whether public cloud or private cloud) to communicate, even if they are located in different countries or even on remote continents. Using a message queue increases fault tolerance and can be used to prevent data being duplicated or lost across geographically and technically disparate systems.
7. Because each service within the system is decoupled, or logically separated from the others, each can continue to function if other services or applications fail or stall.
8. Message queues work across disparate applications such as mobile, IoT and traditional transaction system records. They also support various platforms, such as virtual machines and containers, and can enable integration between legacy applications and today’s latest solutions.
9. Message queues can be used to enable applications and systems residing in different clouds (whether public cloud or private cloud) to communicate, even if they are located in different countries or even on remote continents . Using a message queue increases fault tolerance and can be used to prevent data being duplicated or lost across geographically and technically disparate systems.

## What are popular tools?

Several message queue systems are widely used in the industry:

1. RabbitMQ: A widely-used open-source message broker that supports multiple messaging protocols, including AMQP. It's known for its reliability and extensive features.
2. Apache Kafka: A distributed streaming platform that excels at handling large volumes of data. Kafka is often used for real-time data processing and event streaming.
3. Amazon SQS: A fully managed message queue service provided by AWS. SQS is highly scalable and integrates well with other AWS services.
4. Google Cloud Pub/Sub: A fully managed message queue service offered by Google Cloud, designed for real-time analytics and event-driven applications.
5. Redis Streams: A feature of Redis that provides a simple, in-memory message queue with high performance, suitable for lightweight tasks.
6. ActiveMQ: An open-source message broker that supports various messaging protocols and is used in enterprise environments for reliable messaging.
7. Boomi :Boomi is a cloud-based, on-premise, or hybrid integration platform. It offers a low-code/no-code interface with the capacity for API and EDI connections for integrating with external organizations and systems, as well as compliance with data protection regulations.
8. IBM MQ:IBM MQ (formerly WebSphere MQ and MQSeries) is messaging middleware.
9. IBM Cloud Messages for RabbitMQ:IBM Cloud Messages for RabbitMQ is a managed messaging broker, which supports multiple messaging protocols as a broker that lets you route, track and queue messages with customizable persistence levels, delivery settings and publish confirmations.

## What is Enterprise Message Bus?

1. The EMS Bus Gateway is a small device that provides a link between the EMS bus and a home automation like Domoticz. Just plug in the device to the service jack on the boiler with the supplied jack cable and stick it to the side of the boiler (its magnetic). Or connect it directly to the thermostat wires.
2. No additional cables are needed and everything is powered from the service jack or the thermostat wires itself. All Gateways connect via Wi-Fi to your home network.
3. The Gateway runs the EMS-ESP firmware that communicates via MQTT. When connected to an EMS boiler or heatpump and to a thermostat, solar module, mixer module you can read out many parameters like flow and return temperature and change for instance the setpoint of the thermostat.

EMS device compatibility:

- The EMS interface boards and the EMS Gateways are electrically compatible with all EMS and Heatronic 3 and 4 versions. These include EMS, EMS+, EMS2, EMS Plus, Logamatic EMS, Junkers 2-wire, Heatronic 3, 4. The EMS bus is about 16V.
- **Compatible brands**: Bosch, Nefit, Buderus, Junkers, Worcester, Sieger, elm.leblanc, iVT, Vulcano.
- The support for EMS devices depends on the firmware of the Gateway. Each Gateway is preloaded with a stable or otherwise stable beta version of EMS-ESP32.
- Support for new devices is added with every new release. If your device is not in the list below, it might still be fully or partially compatible. If you are missing parameters you can open an issue on the code repository to get support.

### The assembled EMS Bus Gateway consists of three essential components:

1. A voltage level converter that converts the EMS bus voltage levels to 3.3V TTL levels.
2. A micro-controller.
3. The EMS-ESP32 firmware. <br>

The schematic uses a modified level convertor from the EMS reference schematic circulating the internet. For the micro-controller, a $5 Seeed Studio XIAO ESP32C3 board is used. The micro-controller needs to be programmed with EMS-ESP32 firmware, which is capable of decoding the EMS bus protocol and broadcasting the EMS parameters into your network via MQTT. Finally, the assembled board may be fitted into a Hammond 1551KGY enclosure.

![img](https://github.com/mariusgreuel/EMS-Bus-Gateway/raw/main/docs/ems-bus-gateway-prototype.jpg)

### EMS Bus Background

Many Buderus devices, such as the Buderus Logamax plus GB132 T boiler, use a bus system called EMS (Energy Management System) to communicate with other devices, such as the RC30 room controller.

The EMS bus is a simple two-wire serial bus that uses voltage/current modulation to transmit data. With the proper hardware and software, you can transmit many parameters of your boiler into your home automation system.
