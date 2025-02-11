<a href="https://github.com/cheatsnake/backend-cheats/blob/master/README.md"><p align="center"><img src="./files/logo.png" alt="Logo"/></p></a>

This repository is a visual cheatsheet on the main topics in Backend-development. All the material is divided into topics and subtopics. The structure of the material consists of three parts:

-   **Visual part** - various images/tables/cheatsheets for better understanding (may not be available). All pictures and tables are made from scratch, specifically for this repository.
-   **Summary** - A very brief summary with a list of key terms and concepts. The terms are hyperlinked to the appropriate section on Wikipedia or a similar reference resource.
-   **References to sources** - resources where you may find complete information on a particular issue. If possible, the most authoritative sources are indicated, or those that provide information in as simple and comprehensible language as possible.

> 🛠 The repository is under active development, so it is constantly updated and supplemented

> 🤝 If you want to help the project, feel free to send your [Pull requests](https://github.com/cheatsnake/backend-cheats/pulls)

> 📝 Translation into English is in progress

<p><a name="top"></a></p>

## Contents

<details>
    <summary><a href="#network---internet">1. Network & Internet</a></summary>
    
  * [How the Internet works](#how-the-internet-works)
  * [What is a domain name](#what-is-a-domain-name)
  * [IP address](#ip-address)
  * [What is DNS](#what-is-dns)
  * [Web application design](#web-application-design)
  * [Browsers and how they work](#browsers-and-how-they-work)
  * [VPN and Proxy](#vpn-and-proxy)
  * [Hosting](#hosting)
  * [OSI network model](#osi-network-model)
  * [HTTP Protocol](#http-protocol)
  * [TCP/IP stack](#tcpip-stack)
  * [Network problems](#network-problems)
  * [Network diagnostics](#network-diagnostics)
</details>

<details>
    <summary><a href="#pc-device">2. PC device</a></summary>
    
  * [Main components (hardware)](#main-components--hardware-)
  * [Operating system design](#operating-system-design)
  * [Processes and threads](#processes-and-threads)
  * [Concurrency and parallelism](#concurrency-and-parallelism)
  * [Inter-process communication](#inter-process-communication)
</details>

<details>
    <summary><a href="#linux-basics">3. Linux Basics</a></summary>
    
  * [Working with the terminal](#working-with-the-terminal)
  * [Package manager](#package-manager)
  * [Bash scripts](#bash-scripts)
  * [Users and groups](#users-and-groups)
  * [Permissions](#permissions)
  * [Working with processes](#working-with-processes)
  * [Working with SSH](#working-with-ssh)
  * [Task Scheduler](#task-scheduler)
  * [System logs](#system-logs)
  * [Linux problems](#linux-problems)
</details>

<details>
    <summary><a href="#general-knowledge">4. General knowledge</a></summary>
    
  * [Numeral systems](#numeral-systems)
  * [Logical connective](#logical-connective)
  * [Data structures](#data-structures)
  * [Basic algorithms](#basic-algorithms)
  * [Algorithm complexity](#algorithm-complexity)
  * [Data storage formats](#data-storage-formats)
  * [Text encodings](#text-encodings)
</details>

<details>
    <summary><a href="#programming-language">5. Programming Language</a></summary>
    
  * [Classification of programming languages](#classification-of-programming-languages)
  * [Language Basics](#language-basics)
  * [Server development](#server-development)
  * [Multithreading](#multithreading)
  * [Advanced Topics](#advanced-topics)
  * [Code quality](#code-quality)
</details>

<details>
    <summary><a href="#databases">6. Databases</a></summary>
    
  * [Database classification](#database-classification)
  * [Relational database](#relational-database)
  * [MongoDB](#mongodb)
  * [Redis](#redis)
  * [ACID Requirements](#acid-requirements)
  * [Designing databases](#designing-databases)
</details>

<details>
    <summary><a href="#api-development">7. API development</a></summary>
    
  * [REST API](#rest-api)
  * [GraphQL](#graphql)
  * [WebSockets](#websockets)
  * [RPC and gRPC](#rpc-and-grpc)
  * [WebRTC](#webrtc)
</details>

<details>
    <summary><a href="#software">8. Software</a></summary>
    
  * [Git version control system](#git-version-control-system)
  * [Docker](#docker)
  * [Postman/Insomnia](#postmaninsomnia)
  * [Web servers](#web-servers)
  * [Message brokers](#message-brokers)
</details>

<details>
    <summary><a href="#security">9. Security</a></summary>
    
  * [Web application vulnerabilities](#web-application-vulnerabilities)
  * [Environment variables](#environment-variables)
  * [Hashing](#hashing)
  * [Authentication and authorization](#authentication-and-authorization)
  * [SSL/TLS](#ssltls)
</details>

<details>
    <summary><a href="#testing">10. Testing</a></summary>
    
  * [Unit Tests](#unit-tests)
  * [Integration tests](#integration-tests)
  * [E2E tests](#e2e-tests)
  * [Load testing](#load-testing)
  * [Regression testing](#regression-testing)
</details>

<details>
    <summary><a href="#optimization">11. Optimization</a></summary>

-   [Profiling](#profiling)
-   [Caching](#caching)
-   [Load balancing](#load-balancing)
</details>

<details>
    <summary><a href="#documentation">12. Documentation</a></summary>
    
  * [Markdown](#markdown)
  * [Documentation inside code](#documentation-inside-code)
  * [API Documentation](#api-documentation)
  * [Static generators](#static-generators)
</details>

<details>
    <summary><a href="#building-architecture">13. Building Architecture</a></summary>
    
  * [Architectural templates](#architectural-templates)
  * [Design patterns](#design-patterns)
  * [Monolithic and microservice architecture](#monolithic-and-microservice-architecture)
  * [Horizontal and vertical scaling](#horizontal-and-vertical-scaling)
</details>

[Additional and similar resources](#additional-and-similar-resources)

## Network & Internet

[Internet](https://en.wikipedia.org/wiki/Internet) is a worldwide system that connects computer networks from around the world into a single network for storing/transferring information. The Internet was originally developed for the military. But soon it began to be implemented in universities, and then it could be used by private companies, which began to organize networks of providers that provide Internet access services to ordinary citizens. By early 2020, the number of Internet users exceeded 4.5 billion.

-   ### How the Internet works

    <p align="center"><img src="./files/network-internet/Internet.png" alt="Internet"/></p>

    Your computer has never been directly connected to the Internet. Because it can only see its local network to which other devices are connected via wired ([Ethernet](https://en.wikipedia.org/wiki/Ethernet)) or wirelessly (Wi-Fi, Bluetooth). To communicate with the Internet, you have a special minicomputer in your local network - [router](<https://en.wikipedia.org/wiki/Router_(computing)>). It then connects you to [Internet Service Provider](https://en.wikipedia.org/wiki/Internet_service_provider) which in turn connects to other higher-level providers. Thus, your message, transits through the network of several ISPs before reaching the destination network.

    The Internet is just a long wire to which a small number of [Tier 1 providers](https://en.wikipedia.org/wiki/Tier_1_network) are directly connected. The ISPs below that are just renting access.

    -   [Host](<https://en.wikipedia.org/wiki/Host_(network)>)
        > Any device that is on any network.
    -   [Server](<https://en.wikipedia.org/wiki/Server_(computing)>)
        > A special computer on the network that serves requests from other computers.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How does the Internet work?** – MDN](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work)
2. 📺 [**How does the internet work? (Full Course)** – YouTube](https://youtu.be/zN8YNNHcaZc)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### What is a domain name

    <p align="center"><img src="./files/network-internet/domain_eng.png" alt="Domain name"/></p>

    [Domain Names](https://en.wikipedia.org/wiki/Domain_name) are human-readable addresses of web servers available on the Internet. They consist of parts (levels) separated from each other by a dot. Each of these parts provides specific information about the domain name. For example country, service name, localization, etc.

    -   Who owns domain names
        > [The ICANN Corporation](https://en.wikipedia.org/wiki/ICANN) is the founder of the distributed domain registration system. It gives accreditations to companies that want to sell domains. In this way a competitive domain market is formed.
    -   How to buy a domain name
        > A domain name cannot be bought forever. It is leased for a certain period of time. It is better to buy domains from [accredited registrars](https://www.icann.org/en/accredited-registrars?filter-letter=a&sort-direction=asc&sort-param=name&page=1) (you can find them in almost any country).

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is a Domain Name?** – MDN](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_domain_name)
2. 📺 [**A Beginners Guide to How Domain Names Work!** – YouTube](https://youtu.be/Y4cRx19nhJk)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### IP address

    <p align="center"><img src="./files/network-internet/IPv4-IPv6.png" alt="IPv4-IPv6"/></p>

    [IP address](https://en.wikipedia.org/wiki/IP_address) is a unique numeric address that is used to recognize a particular device on the network.

    -   Levels of visibility
        > -   External and publicly accessible IP address that belongs to your ISP and is used to access the Internet by hundreds of other users.
        > -   The IP address of your router in your ISP's local network, the same IP address from which you access the Internet.
        > -   The IP address of your computer in the local (home) network created by the router, to which you can connect your devices. Typically, it looks like 192.168.XXX.XXX.
        > -   The internal IP address of the computer, inaccessible from the outside and used only for communication between the running processes. It is the same for everyone - 127.0.0.1 or just _localhost_.
    -   [Port](<https://en.wikipedia.org/wiki/Port_(computer_networking)>)
        > One device (computer) can run many applications that use the network. In order to correctly recognize where and which data coming over the network should be delivered (to which of the applications) a special numerical number - a port is used. That is, each running process on a computer which uses a network connection has its own personal port.
    -   [IPv4](https://en.wikipedia.org/wiki/IPv4)
        > Version 4 of the IP protocol. It was developed in 1981 and limits the address space to about 4.3 billion (2^32) possible unique addresses.
    -   [IPv6](https://en.wikipedia.org/wiki/IPv6)
        > Over time, the allocation of address space began to happen at a much faster rate, forcing the creation of a new version of the IP protocol to store more addresses. IPv6 is capable of issuing 2^128 (is huge number) unique addresses.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**IP addresses. Explained** – YouTube](https://youtu.be/7_-qWlvQQtY)
2. 📺 [**Public IP vs. Private IP and Port Forwarding (Explained by Example)** – YouTube](https://youtu.be/92b-jjBURkw)
3. 📺 [**What is IP address and types of IP address - IPv4 and IPv6** – YouTube](https://youtu.be/8npT9AALbrI)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### What is DNS

    <p align="center"><img src="./files/network-internet/dns.png" alt="DNS"/></p>

    [DNS (Domain Name System)](https://en.wikipedia.org/wiki/DNS) is a decentralized Internet address naming system that allows you to create human-readable alphabetic names (domain names) corresponding to the numeric [IP addresses](#ip-address) used by computers.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is DNS? Domain Name System explained** – freeCodeCamp](https://www.freecodecamp.org/news/what-is-dns/)
2. 📺 [**DNS (Domain Name System) explained. Types of Domain Name Servers** – YouTube](https://youtu.be/JkEYOt08-rU)
3. 📺 [**DNS as Fast As Possible** – YouTube](https://youtu.be/Rck3BALhI5c)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Web application design

    Modern [web applications](https://en.wikipedia.org/wiki/Web_application) consist of two parts: [Frontend and Backend](https://en.wikipedia.org/wiki/Frontend_and_backend). Thus implementing a [client-server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model).

    The tasks of the Frontend are:

    -   Implementation of the user interface (appearance of the application)
        > A special markup language [HTML](https://en.wikipedia.org/wiki/HTML) is used to create web pages. <br> > [CSS](https://en.wikipedia.org/wiki/CSS) style language is used to style fonts, layout of content, etc. <br> > [JavaScript](https://en.wikipedia.org/wiki/JavaScript) programming language is used to add dynamics and interactivity. <br>
        > As a rule, these tools are rarely used in their pure form, as so-called [frameworks](https://2020.stateofjs.com/en-US/technologies/front-end-frameworks/) and [preprocessors](https://www.freecodecamp.org/news/css-preprocessors/) exist for more convenient and faster development. <br>
    -   Creating functionality for generating requests to the server
        > These are usually different types of input forms that can be conveniently interacted with.
    -   Receives data from the server and then processes it for output to the client

    Tasks of the Backend:

    -   Handling client requests
        > Checking for permissions and access, all sorts of validations, etc.
    -   Implementing business logic
        > A wide range of tasks can be implied here: working with databases, information processing, computation, etc. This is, so to speak, the heart of the Backend world. This is where all the important and interesting stuff happens.
    -   Generating a response and sending it to the client

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Front-End vs. Back-End explained**](https://blog.teamtreehouse.com/i-dont-speak-your-language-frontend-vs-backend)
2. 📺 [**Everything You NEED to Know About WEB APP Architecture** – YouTube](https://youtu.be/sDlCSIDwpDs)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Browsers and how they work

    <p align="center"><img src="./files/network-internet/browser_eng.png" alt="Browser"/></p>

    [Browser](https://en.wikipedia.org/wiki/Web_browser) is a client which can be used to send requests to a server for files which can then be used to render web pages. In simple terms, a browser can be thought of as a program for viewing HTML files, which can also search for and download them from the Internet.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How browsers work** – MDN](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)
2. 📄 [**How browsers work: Behind the scenes of modern web browsers** – web.dev](https://web.dev/howbrowserswork/)
3. 📺 [**What is a web browser?** – YouTube](https://youtu.be/QzohDuGk4mM)
4. 📺 [**Anatomy of the browser 101 (Chrome University 2019)** – YouTube](https://youtu.be/PzzNuCk-e0Y)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### VPN and Proxy

    <p align="center"><img src="./files/network-internet/proxy-vpn_eng.png" alt="Proxy & VPN"/></p>

    The use of VPNs and Proxy is quite common in recent years. With the help of these technologies, users can get basic anonymity when surfing the web, as well as bypass various regional blockages.

    -   [VPN (Virtual Private Network)](https://en.wikipedia.org/wiki/VPN)
        > A technology that allows you to become a member of a private network (similar to your local network), where requests from all participants go through a single public IP address. This allows you to blend in with the general mass of requests from other participants. <br>
        >
        > -   Simple procedure for connection and use. <br>
        > -   Reliable traffic encryption. <br>
        > -   There is no guarantee of 100% anonymity, because the owner of the network knows the IP-addresses of all participants. <br>
        > -   VPNs are useless for dealing with multi-accounts and some programs because all accounts operating from the same VPN are easily detected and blocked. <br>
        > -   Free VPNs tend to be heavily loaded, resulting in unstable performance and slow download speeds. <br>
    -   [Proxy (proxy server)](https://en.wikipedia.org/wiki/Proxy_server)
        > A proxy is a special server on the network that acts as an intermediary between you and the destination server you intend to reach. When you are connected to a proxy server all your requests will be performed on behalf of that server, that is, your IP address and location will be substituted. <br>
        >
        > -   The ability to use an individual IP address, which allows you to work with multi-accounts. <br>
        > -   Stability of the connection due to the absence of high loads. <br>
        > -   Connection via proxy is provided in the operating system and browser, so no additional software is required. <br>
        > -   There are proxy varieties that provide a high level of anonymity. <br>
        > -   The unreliability of free solutions, because the proxy server can see and control everything you do on the Internet. <br>

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is VPN? How It Works, Types of VPN** – kaspersky.com](https://www.kaspersky.com/resource-center/definitions/what-is-a-vpn)
2. 📺 [**What Is a Proxy and How Does It Work?** – YouTube](https://youtu.be/ayo2EUPTEkE)
3. 📺 [**Proxy vs. Reverse Proxy (Explained by Example)** – YouTube](https://youtu.be/ozhe__GdWC8)
4. 📺 [**VPN vs Proxy Explained Pros and Cons** – YouTube](https://youtu.be/npnqyRT77Zc)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Hosting

    <p align="center"><img src="./files/network-internet/Hosting.png" alt="Hosting"/></p>

    [Hosting](https://en.wikipedia.org/wiki/Web_hosting_service) is a special [service provided](https://en.wikipedia.org/wiki/Internet_hosting_service) by hosting providers, which allows you to rent space on a server (which is connected to the Internet around the clock), where your data and files can be stored. There are different options for hosting, where you can use not only the disk space of the server, but also the CPU power to run your network applications.

    -   [Virtual hosting](https://en.wikipedia.org/wiki/Virtual_hosting)
        > One physical server that distributes its resources to multiple tenants.
    -   [VPS/VDS](https://en.wikipedia.org/wiki/Virtual_private_server)
        > Virtual servers that emulate the operation of a separate physical server and are available for rent to the client with maximum privileges.
    -   [Dedicated server](https://en.wikipedia.org/wiki/Dedicated_hosting_service)
        > Renting a full physical server with full access to all resources. As a rule, this is the most expensive service.
    -   [Cloud hosting](https://en.wikipedia.org/wiki/Cloud_storage)
        > A service that uses the resources of several servers. When renting, the user pays only for the actual resources used.
    -   [Colocation](https://en.wikipedia.org/wiki/Colocation_centre)
        > A service that gives the customer the opportunity to install their equipment on the provider's premises.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is Web Hosting?** – namecheap.com](https://www.namecheap.com/hosting/what-is-web-hosting-definition/)
2. 📺 [**What is Web Hosting and How Does It Work?** – YouTube](https://youtu.be/H8oAvyqQwew)
3. 📺 [**Different Hosting Types Explained** – YouTube](https://youtu.be/CtNWVmt9U1M)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### OSI network model

    | №   | Level              | Used protocols       |
    | --- | ------------------ | -------------------- |
    | 7   | Application layer  | HTTP, DNS, FTP, POP3 |
    | 6   | Presentation layer | SSL, SSH, IMAP, JPEG |
    | 5   | Session layer      | APIs Sockets         |
    | 4   | Transport layer    | TCP, UDP             |
    | 3   | Network layer      | IP, ICMP, IGMP       |
    | 2   | Data link layer    | Ethernet, MAC, HDLC  |
    | 1   | Physical layer     | RS-232, RJ45, DSL    |

    -   [Physical layer](https://en.wikipedia.org/wiki/Physical_layer)
        > At this level, bits (ones/zeros) are encoded into physical signals (current, light, radio waves) and transmitted further by wire ([Ethernet](https://en.wikipedia.org/wiki/Ethernet)) or wirelessly ([Wi-Fi](https://en.wikipedia.org/wiki/Wi-Fi)).
    -   [Data link layer](https://en.wikipedia.org/wiki/Data_link_layer)
        > Physical signals from layer 1 are decoded back into ones and zeros, errors and defects are corrected, and the sender and receiver [MAC addresses](https://en.wikipedia.org/wiki/MAC_address) are extracted.
    -   [Network layer](https://en.wikipedia.org/wiki/Network_layer)
        > This is where traffic routing, DNS queries and [IP packet](https://en.wikipedia.org/wiki/Internet_Protocol) generation take place.
    -   [Transport layer](https://en.wikipedia.org/wiki/Transport_layer)
        > The layer responsible for data transfer. There are two important protocols: <br>
        >
        > -   [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) is a protocol that ensures reliable data transmission. TCP guarantees data delivery and preserves the order of the messages. This has an impact on the transmission speed. This protocol is used where data loss is unacceptable, such as when sending mail or loading web pages. <br>
        > -   [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) is a simple protocol with fast data transfer. It does not use mechanisms to guarantee the delivery and ordering of data. It is used e.g. in online games where partial packet loss is not crucial, but the speed of data transfer is much more important. Also, requests to DNS servers are made through UDP protocol.
    -   [Session layer](https://en.wikipedia.org/wiki/Session_layer)
        > Responsible for opening and closing communications (sessions) between two devices. Ensures that the session stays open long enough to transfer all necessary data, and then closes quickly to avoid wasting resources.
    -   [Presentation layer](https://en.wikipedia.org/wiki/Presentation_layer)
        > Transmission, encryption/decryption and data compression. This is where data that comes in the form of zeros and ones are converted into desired formats (PNG, MP3, PDF, etc.)
    -   [Application layer](https://en.wikipedia.org/wiki/Application_layer)
        > Allows the user's applications to access network services such as database query handler, file access, email forwarding.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Layers of OSI Model** – geeksForGeeks](https://www.geeksforgeeks.org/layers-of-osi-model/)
2. 📺 [**The OSI Model - Explained by Example** – YouTube](https://youtu.be/7IS7gigunyI)
3. 📺 [**TCP vs UDP Crash Course** – YouTube](https://youtu.be/qqRYkcta6IE)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### HTTP Protocol

    [HTTP (HyperText Transport Protocol)](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) is the most important protocol on the Internet. It is used to transfer data of any format. The protocol itself works according to a simple principle: request -> response.

    -   [Structure of HTTP messages](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)
        > Start Line > Headers > Message Body

    <p align="center"><img src="./files/network-internet/http_eng.png" alt="HTTP"/></p>

    -   [Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
        > Additional service information that is sent with the request/response. <br>
        > Common headers: [Host](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Host), [User-Agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent), [If-Modified-Since](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/If-Modified-Since), [Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cookie), [Referer](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer), [Authorization](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization), [Cache-Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control), [Content-Type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type), [Content-Length](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Length), [Last-Modified](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Last-Modified), [Set-Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie), [Content-Encoding](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Encoding).
    -   [Request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
        > [GET](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET) - data retrieval request <br> [POST](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST) - request with data to create a new record <br> [PUT](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT) - request with data to change existing record <br> [DELETE](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE) - deletion request <br> Others: [HEAD](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD), [CONNECT](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/CONNECT), [OPTIONS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS), [TRACE](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/TRACE), [PATCH](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PATCH). <br>
    -   [Response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
        > Each response from the server has a special numeric code that characterizes the state of the sent request. These codes are divided into 5 main classes:
        >
        > -   1хх - service information <br>
        > -   2хх - successful request <br>
        > -   3хх - redirect to another address <br>
        > -   4хх - client side error <br>
        > -   5хх - server side error <br>
    -   [HTTPS](https://developer.mozilla.org/en-US/docs/Glossary/https)
        > Same HTTP, but with encryption support
    -   [Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
        > Because the HTTP protocol does not allow you to save any information about the status of previous requests/responses, you need to use cookies. Cookies allow the server to store various information on the client side, which the client can then send back to the server. In particular, cookies can be used for authorization or to save various settings/configurations.
    -   [CORS (Cross origin resource sharing)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
        > A technology that allows one domain to securely receive data from another domain.
    -   [CSP (Content Security Policy)](https://developer.mozilla.org/ru/docs/Web/HTTP/CSP)
        > A special header that allows you to recognize and eliminate certain types of web application vulnerabilities.
    -   [HTTP/1.0 vs HTTP/1.1 vs HTTP/2](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Persistent_connections)
        > The main innovation in version 1.1 is the permanent connection mode, which allows you to send several requests per connection. In version 2, the protocol became binary, with the ability to transmit data from multiple streams on the same channel.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How HTTP Works and Why it's Important** – freeCodeCamp](https://www.freecodecamp.org/news/how-the-internet-works/)
2. 📄 [**Hypertext Transfer Protocol (HTTP)** – MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP)
3. 📺 [**Hyper Text Transfer Protocol Crash Course** – YouTube](https://youtu.be/0OrmKCB0UrQ)
4. 📄 [**HTTP vs HTTPS – What's the Difference?** – freeCodeCamp](https://www.freecodecamp.org/news/http-vs-https/)
5. 📺 [**HTTP Cookies Crash Course** – YouTube](https://youtu.be/sovAIX4doOE)
6. 📺 [**Cross Origin Resource Sharing (Explained by Example)** – YouTube](https://youtu.be/Ka8vG5miErk)
7. 📺 [**When to use HTTP GET vs POST?** – YouTube](https://youtu.be/K8HJ6DN23zI)
8. 📺 [**How HTTP/2 Works, Performance, Pros & Cons and More** – YouTube](https://youtu.be/fVKPrDrEwTI)
9. 📺 [**HTTP/2 Critical Limitation that led to HTTP/3 & QUIC** – YouTube](https://youtu.be/GriONb4EfPY)
10. 📺 [**304 Not Modified HTTP Status (Explained with Code Example and Pros & Cons)** – YouTube](https://youtu.be/0QHmHR55_Lo)
11. 📺 [**What is the Largest POST Request the Server can Process?** – YouTube](https://youtu.be/0QHmHR55_Lo)
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### TCP/IP stack

    <p align="center"><img src="./files/network-internet/tcp-ip_eng.png" alt="TCP/IP"/></p>

    Compared to the [OSI model](https://github.com/cheatsnake/backend-cheats/blob/master/README_ENG.md#osi-network-model), the [TCP/IP](https://en.wikipedia.org/wiki/Internet_protocol_suite) stack has a simpler architecture. It is widely used and was first used as the basis for the creation of a global network, and then to describe the workings of the Internet.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is the TCP/IP Model? Layers and Protocols Explained** – freeCodeCamp](https://www.freecodecamp.org/news/what-is-tcp-ip-layers-and-protocols-explained/)
2. 📺 [**What is TCP/IP?** – YouTube](https://youtu.be/PpsEaqJV_A0)
3. 📺 [**How TCP really works. Three-way handshake. TCP/IP Deep Dive** – YouTube](https://youtu.be/rmFX1V49K8U)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Network problems

    <p align="center"><img src="./files/network-internet/problems_eng.gif" alt="Problems"/></p>

    The quality of networks, much less the Internet, is far from ideal. This is due to the complex and dispersed network structure in different devices. Therefore, on the functioning of the network affects a huge number of factors. For example: the stability of the connection between the client device and its router, the quality of service of the provider, the power and performance of the server, the physical distance between the client and the server, etc.

    -   [Latency](https://developer.mozilla.org/en-US/docs/Web/Performance/Understanding_latency)
        > The time it takes for a data packet to travel from sender to receiver. It depends more on the physical distance.
    -   [Packet loss](https://en.wikipedia.org/wiki/Packet_loss)
        > Not all packets traveling over the network can reach their destination. This happens most often when using wireless networks or due to [network congestion](https://en.wikipedia.org/wiki/Network_congestion).
    -   [Round Trip Time (RTT)](https://en.wikipedia.org/wiki/Round-trip_delay)
        > The time it takes for the data packet to reach its destination + the time to respond that the packet was received successfully.
    -   [Jitter](https://www.ir.com/guides/what-is-network-jitter)
        > Delay fluctuations, unstable ping (for example, 50ms, 120ms, 35ms...).
    -   [Packet reordering](https://wiki.geant.org/display/public/EK/PacketReordering)
        > The IP protocol does not guarantee that packets are delivered in the order in which they are sent.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Understanding latency** – MDN](https://developer.mozilla.org/en-US/docs/Web/Performance/Understanding_latency)
2. 📺 [**What is latency? What affects latency?** – YouTube](https://youtu.be/epAXDsq5SbE)
3. 📺 [**Basics of network bandwidth, latency, and jitter** – YouTube](https://youtu.be/WdbJdUh6W08)
4. 📺 [**Round Trip Time (RTT)** – YouTube](https://youtu.be/nT9F-USjtBg)
5. 📺 [**What Causes Packet Loss and How to Eliminate It In Your Network** – YouTube](https://youtu.be/Cg656nGbXe4)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Network diagnostics

    <p align="center"><img src="./files/network-internet/Traceroute.png" alt="Traceroute"/></p>

    -   [Traceroute](https://en.wikipedia.org/wiki/Traceroute)
        > A procedure that allows you to trace to which nodes, with which IP addresses, a packet you send before it reaches its destination. Tracing can be used to identify computer network related problems and to examine/analyze the network.
    -   [Ping scan](<https://en.wikipedia.org/wiki/Ping_(networking_utility)>)
        > The easiest way to check the server for performance.
    -   [Checking for packet loss](https://www.dnsstuff.com/packet-loss-test)
        > Due to dropped connections, not all packets sent over the network reach their destination.
    -   [Wireshark](https://en.wikipedia.org/wiki/Wireshark)
        > A powerful program with a graphical interface for analyzing all traffic that passes through the network in real time.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**How does traceroute work?** – YouTube](https://youtu.be/G05y9UKT69s)
2. 📺 [**Traceroute (tracert) Explained - Network Troubleshooting** – YouTube](https://youtu.be/up3bcBLZS74)
3. 📺 [**Nmap - Host Discovery With Ping Sweep** – YouTube](https://youtu.be/LvCDaftsMwI)
4. 📺 [**Internet Troubleshooting - Pathping Packet Loss** – YouTube](https://youtu.be/VPdotNIXOgI)
5. 📺 [**Wireshark crash course (playlist)** – YouTube](https://youtube.com/playlist?list=PLBf0hzazHTGPgyxeEj_9LBHiqjtNEjsgt)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## PC device

-   ### Main components (hardware)

    -   [Motherboard](https://en.wikipedia.org/wiki/Motherboard)
        > The most important PC component to which all other elements are connected.
        >
        > -   [Chipset](https://en.wikipedia.org/wiki/Chipset) - set of electronic components that responsible for the communication of all motherboard components.
        > -   [CPU socket](https://en.wikipedia.org/wiki/CPU_socket) - socket for mounting the processor.
        > -   [VRM (Voltage Regulator Module)](https://en.wikipedia.org/wiki/Voltage_regulator_module) – module that converts the incoming voltage (usually 12V) to a lower voltage to run the processor, integrated graphics, memory, etc.
        > -   Slots for RAM.
        > -   Expansion slots [PCI-Express](https://en.wikipedia.org/wiki/PCI_Express) - designed for connection of video cards, external network/sound cards.
        > -   Slots [М.2](https://en.wikipedia.org/wiki/M.2) / [SATA](https://en.wikipedia.org/wiki/SATA) - designed to connect hard disks and SSDs.
    -   [CPU (Central processing unit)](https://en.wikipedia.org/wiki/Central_processing_unit)
        > The most important device that executes instructions (programme code). Processors only work with 1 and 0, so all programmes are ultimately a set of binary code.
        >
        > -   [Registers](https://en.wikipedia.org/wiki/Processor_register) - the fastest memory in a PC, has an extremely small capacity, is built into the processor and is designed to temporarily store the data being processed.
        > -   [Cache](https://en.wikipedia.org/wiki/CPU_cache) - slightly less fast memory, which is also built into the processor and is used to store a copy of data from frequently used cells in the main memory.
        > -   Processors can have different [architectures](https://en.wikipedia.org/wiki/Processor_design). Currently, the most common are the [x86](https://en.wikipedia.org/wiki/X86-64) architecture (desktop and laptop computers) and [ARM](https://en.wikipedia.org/wiki/ARM_architecture_family) (mobile devices as well as the latest Apple computers).
    -   [RAM (Random-access memory)](https://en.wikipedia.org/wiki/Random-access_memory)
        > Fast, low capacity memory (4-16GB) designed to temporarily store program code, as well as input, output and intermediate data processed by the processor.
    -   [Data storage](https://en.wikipedia.org/wiki/Data_storage)
        > Large capacity memory (256GB-1TB) designed for long-term storage of files and installed programmes.
    -   [GPU (Graphics card)](https://en.wikipedia.org/wiki/Graphics_card)
        > A separate card that translates and processes data into images for display on a monitor. This device is also called a discrete graphics card. Usually needed for those who do 3D modelling or play games. <br> > [Built-in graphics card](https://en.wikipedia.org/wiki/Graphics_processing_unit#Integrated_graphics_processing_unit) is a graphics card built into the processor. It is suitable for daily work.
    -   [Network card](https://en.wikipedia.org/wiki/Network_interface_controller)
        > A device that receives and transmits data from other devices connected to the [local network](https://en.wikipedia.org/wiki/Local_area_network).
    -   [Sound card](https://en.wikipedia.org/wiki/Sound_card)
        > A device that allows you to process sound, output it to other devices, record it with a microphone, etc.
    -   [Power supply unit](<https://en.wikipedia.org/wiki/Power_supply_unit_(computer)>)
        > A device designed to convert the AC voltage from the mains to DC voltage.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Everything You Need to Know About Computer Hardware**](https://www.lifewire.com/computer-hardware-2625895)
2. 📺 [**What does what in your computer? Computer parts Explained** – YouTube](https://youtu.be/ExxFxD4OSZ0)
3. 📺 [**The Fetch-Execute Cycle: What's Your Computer Actually Doing?** – YouTube](https://youtu.be/Z5JC9Ve1sfI)
4. 📺 [**How a CPU Works in 100 Seconds // Apple Silicon M1 vs Intel i9** – YouTube](https://youtu.be/vqs_0W-MSB0)
5. 📺 [**Arm vs x86 - Key Differences Explained** – YouTube](https://youtu.be/AADZo73yrq4)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Operating system design

    <p align="center"><img src="./files/os/os-layer_eng.png" alt="OS"/></p>

    [Operating system (OS)](https://en.wikipedia.org/wiki/Operating_system) is a comprehensive software system designed to manage a computer's resources. With operating systems, people do not have to deal directly with the processor, RAM or other parts of the PC.

    OS can be thought of as an abstraction layer that manages the hardware of a computer, thereby providing a simple and convenient environment for user software to run.

    -   Main features
        > -   RAM management (space allocation for individual programms)
        > -   Loading programms into RAM and their execution
        > -   Execution of requests from user's programms (inputting and outputting data, starting and stopping other programms, freeing up memory or allocating additional memory, etc.)
        > -   Interaction with input and output devices (mouse, keyboard, monitor, etc.)
        > -   Interaction with storage media (HDDs and SSDs)
        > -   Providing a user's interface (console shell or graphical interface)
        > -   Logging of software errors (saving logs)
    -   Additional functions (may not be available in all OSs)
        > -   Organise [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) (simultaneous execution of several programms)
        > -   Delimiting access to resources for each process
        > -   [Inter-process communication](https://en.wikipedia.org/wiki/Inter-process_communication) (data exchange, synchronisation)
        > -   Organise the protection of the operating system itself against other programms and the actions of the user
        > -   Provide multi-user mode and differentiate rights between different OS users (admins, guests, etc.)
    -   [OS kernel](<https://en.wikipedia.org/wiki/Kernel_(operating_system)>)
        > The central part of the operating system which is used most intensively. The kernel is constantly in memory, while other parts of the OS are loaded into and unloaded from memory as needed.
    -   [Bootloader](https://en.wikipedia.org/wiki/Bootloader)
        > The system software that prepares the environment for the OS to run (puts the hardware in the right state, prepares the memory, loads the OS kernel there and transfers control to it (the kernel).
    -   [Device drivers](https://en.wikipedia.org/wiki/Device_driver)
        > Special software that allows the OS to work with a particular piece of equipment.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is an OS? Operating System Definition for Beginners** – freeCodeCamp](https://www.freecodecamp.org/news/what-is-an-os-operating-system-definition-for-beginners/)
2. 📄 [**Windows vs MacOS vs Linux – Operating System Handbook** – freeCodeCamp](https://www.freecodecamp.org/news/an-introduction-to-operating-systems/)
3. 📺 [**Operating Systems: Crash Course Computer Science** – YouTube](https://youtu.be/26QPDBe-NB8)
4. 📺 [**Operating System Basics** – YouTube](https://youtu.be/9GDX-IyZ_C8)
5. 📺 [**Operating System in deep details (playlist)** – YouTube](https://youtube.com/playlistlist=PLBlnK6fEyqRiVhbXDGLXDk_OQAeuVcp2O)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Processes and threads

    <p align="center"><img src="./files/os/process_eng.png" alt="Process"/></p>

    -   [Process](<https://en.wikipedia.org/wiki/Process_(computing)>)
        > A kind of container in which all the resources needed to run a program are stored. As a rule, the process consists of:
        >
        > -   Executable program code <br>
        > -   Input and output data <br>
        > -   [Call stack](https://en.wikipedia.org/wiki/Call_stack) (order of instructions for execution) <br>
        > -   [Heap](https://en.wikipedia.org/wiki/Memory_management#Manual_memory_management) (a structure for storing intermediate data created during the process) <br>
        > -   [Segment descriptor](https://en.wikipedia.org/wiki/Segment_descriptor) <br>
        > -   [File descriptor](https://en.wikipedia.org/wiki/File_descriptor) <br>
        > -   Information about the set of permissible powers <br>
        > -   Processor status information
    -   [Thread](<https://en.wikipedia.org/wiki/Thread_(computing)>)
        > An entity in which sequences of program actions (procedures) are executed. Threads are within a process and use the same address space. There can be multiple threads in a single process, allowing multiple tasks to be performed. These tasks, thanks to threads, can exchange data, use shared data or the results of other tasks.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**Difference Between Process and Thread** – YouTube](https://youtu.be/O3EyzlZxx3g)
2. 📺 [**How Do CPUs Use Multiple Cores** – YouTube](https://youtu.be/S3I5WNHbnJ0)
3. 📺 [**What is Hyper Threading Technology** – YouTube](https://youtu.be/wnS50lJicXc)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Concurrency and parallelism

    <p align="center"><img src="./files/os/concurrency-parallel.png" alt="Concurrency-parallelism"/></p>

    -   [Parallelism](https://en.wikipedia.org/wiki/Parallel_computing)
        > The ability to perform multiple tasks simultaneously using multiple processor cores, where each individual core performs a different task.
    -   [Concurrency](<https://en.wikipedia.org/wiki/Concurrency_(computer_science)>)
        > The ability to perform multiple tasks, but using a single processor core. This is achieved by dividing tasks into separate blocks of commands which are executed in turn, but switching between these blocks is so fast that for users it seems as if these processes are running simultaneously.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Concurrency, parallelism, and the many threads of Santa Claus** – freeCodeCamp](https://www.freecodecamp.org/news/concurrency-parallelism-and-the-many-threads-of-santa-claus/)
2. 📺 [**Concurrency vs Parallelism** – YouTube](https://youtu.be/Y1pgpn2gOSg)
3. 📺 [**Concurrency is not Parallelism by Rob Pike** – YouTube](https://youtu.be/oV9rvDllKEg)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Inter-process communication

    A mechanism which allows to exchange data between threads of one or different processes. Processes can be run on the same computer or on different computers connected by a network. [Inter-process communication](https://en.wikipedia.org/wiki/Inter-process_communication) can be done in different ways.

    -   [File](https://en.wikipedia.org/wiki/Computer_file)
        > The easiest way to exchange data. One process writes data to a certain file, another process reads the same file and thus receives data from the first process.
    -   [Signal (IPC)](<https://en.wikipedia.org/wiki/Signal_(IPC)>)
        > Asynchronous notification of one process about an event which occurred in another process.
    -   [Network socket](https://en.wikipedia.org/wiki/Network_socket)
        > In particular, IP addresses and ports are used to communicate between computers using the TCP/IP protocol stack. This pair defines a socket (_socket_ corresponding to the address and port).
    -   [Semaphore](<https://en.wikipedia.org/wiki/Semaphore_(programming)>)
        > A counter over which only 2 operations can be performed: increasing and decreasing (and for 0 the decreasing operation is blocked).
    -   [Message passing](https://en.wikipedia.org/wiki/Message_passing) & [Message queue](https://en.wikipedia.org/wiki/Message_queue)
    -   [Pipelines](<https://en.wikipedia.org/wiki/Pipeline_(Unix)>)
        > Redirecting the output of one process to the input of another (similar to a pipe).

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Interprocess Communications** – Microsoft](https://learn.microsoft.com/en-us/windows/win32/ipc/interprocess-communications)
2. 📺 [**Interprocess Communication** – YouTube](https://youtu.be/dJuYKfR8vec)
3. 📺 [**Inter Process Communication** – YouTube](https://youtu.be/W0BX6geRCDQ)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Linux Basics

Operating systems based on [Linux kernel](https://en.wikipedia.org/wiki/Linux_kernel) are the standard in the world of server development, since most servers run on such operating systems. Using Linux on servers is profitable because it is free.

There are a huge number of Linux distributions (preinstalled software bundles) to suit all tastes. One of the most popular is [Ubuntu](https://en.wikipedia.org/wiki/Ubuntu). This is where you can start your dive into server development.

[Install Ubuntu](https://ubuntu.com/download/desktop) on a separate PC or laptop. If this is not possible, you can use a special program [Virtual Box](https://www.virtualbox.org/wiki/Downloads) where you can [run other OS]() on top of the main OS. You can also run [Docker](https://www.docker.com/products/docker-desktop) [Ubuntu image container](https://hub.docker.com/_/ubuntu) (Docker is a [separate topic](#docker) that is exists in this repository).

-   ### Working with the terminal

    [Terminal](https://en.wikipedia.org/wiki/Computer_terminal) is a program that uses special text commands to control your computer. Generally, servers do not have graphical interfaces, so you will definitely need terminal skills.

    -   Basic commands for navigating the file system
        ```bash
        ls # list directory contents
        cd <path> # go to specified directory
        cd .. # move to a higher level (to the parent directory)
        touch <file> # create a file
        cat > <file> # enter text into the file (overwrite)
        cat >> <file> # enter text at the end of the file (append)
        cat/more/less <file> # to view the file contents
        head/tail <file> # view the first/last lines of a file
        pwd # print path to current directory
        mkdir <name> # create a directory
        rmdir <name> # delete a directory
        cp <file> <path> # copy a file or directory
        mv <file> <path># moving or renaming
        rm <file> # deleting a file or directory
        find <string># file system search
        du <file># output file or directory size
        ```
    -   Commands for help information
        ```bash
        man <command> # allows you to view a manual for any command
        apropos <string> # search for a command with a description that has a specified word
        man -k <string> # similar to the command above
        whatis <command> # a brief description of the command
        ```
    -   Super user rights
        > Analogue to running as administrator in Windows
        ```bash
        sudo <command> # executes a command with superuser privileges
        ```
    -   Text editor
        > Study any in order to read and edit files freely through the terminal.
        > The easiest – [nano](https://en.wikipedia.org/wiki/GNU_nano).
        > The most advanced – [Vim](<https://en.wikipedia.org/wiki/Vim_(text_editor)>).

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**31 Linux Commands Every Ubuntu User Should Know**](https://itsfoss.com/essential-ubuntu-commands/)
2. 📄 [**The Linux Command Handbook** – freeCodeCamp](https://www.freecodecamp.org/news/the-linux-commands-handbook/)
3. 📺 [**The 50 Most Popular Linux & Terminal Commands** – YouTube](https://youtu.be/ZtqBQ68cfJc)
4. 📺 [**Nano Editor Fundamentals** – YouTube](https://youtu.be/gyKiDczLIZ4)
5. 📺 [**Vim Tutorial for Beginners** – YouTube](https://youtu.be/RZ4p-saaQkc)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Package manager

    The Package Manager is a utility that allows you to install/update software packages from the terminal.

    Linux distributions can be divided into several groups, depending on which package manager they use: [apt](<https://en.wikipedia.org/wiki/APT_(software)>) (in [Debian](https://en.wikipedia.org/wiki/Debian) based distributions), [RPM](https://en.wikipedia.org/wiki/RPM_Package_Manager) (the [Red Hat](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux) package management system) and [Pacman](https://en.wikipedia.org/wiki/Arch_Linux#Pacman) (the package manager in [Arch-like distributions](https://en.wikipedia.org/wiki/Arch_Linux))

    Ubuntu is based on Debian, so it uses apt (advanced packaging tool) package manager.

    -   Basic Commands
        ```bash
        apt install <package> # install the package
        apt remove <package> # remove the package, but keep the configuration
        apt purge <package> # remove the package along with the configuration
        apt update # update information about new versions of packages
        apt upgrade # update the packages installed in the system
        apt list --installed # list of packages installed on the system
        apt list --upgradable # list of packages that need to be updated
        apt search <package> # searching for packages by name on the network
        apt show <package> # package information
        ```

<details>
    <summary>🔗 <b>References</b></summary>
    
1. 📺 [**Linux Crash Course - The apt Command** – YouTube](https://youtu.be/1kicKTbK768)
2. 📺 [**Linux Package Management | Debian, Fedora, and Arch Linux** – YouTube](https://youtu.be/lkii2cGuKao)
3. 📄 [**sudo apt-get update vs upgrade – What is the Difference?** – freeCodeCamp](https://www.freecodecamp.org/news/sudo-apt-get-update-vs-upgrade-what-is-the-difference)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Bash scripts

    You can use scripts to automate the sequential input of any number of commands. In [Bash](<https://en.wikipedia.org/wiki/Bash_(Unix_shell)>) you can create different conditions (branching), loops, timers, etc. to perform all kinds of actions related to console input.

    -   [Basics of Bash Scripts](./files/linux/bash-scripts-cheatsheet.md)
        > The most basic and frequently used features such as: variables, I/O, loops, conditions, etc.
    -   Practice
        > Solve challenges on sites like [HackerRank](https://www.hackerrank.com/domains/shell) and [Codewars](https://www.codewars.com/join?language=shell).
        > Start using Bash to automate routine activities on your computer. If you're already a programmer, create scripts to easily build your project, to install settings, and so on.
    -   [ShellCheck](https://github.com/koalaman/shellcheck) script analysis tool
        > It will point out possible mistakes and teach you best practices for writing really good scripts.
    -   Additional resources
        > Repositories such as [awesome bash](https://github.com/awesome-lists/awesome-bash) and [awesome shell](https://github.com/alebcay/awesome-shell) have entire collections of useful resources and tools to help you develop even more skills with Bash and the terminal in general.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Shell Scripting for Beginners** – freeCodeCamp](https://www.freecodecamp.org/news/shell-scripting-crash-course-how-to-write-bash-scripts-in-linux/)
2. 📺 [**Bash Scripting Full Course 3 Hours** – YouTube](https://youtu.be/e7BufAVwDiM)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Users and groups

    Linux-based operating systems are multi-user. This means that several people can run many different applications at the same time on the same computer. For the Linux system to be able to "recognize" a user, he must be logged in and therefore each user must have a unique name and a secret password.

    -   Working with users
        ```bash
        useradd <name> [flags] # create a new user
        passwd <name> # set a password for the user
        usermod <name> [flags] # edit a user
        usermod -L <name> # block a user
        usermod -U <name> # unblock a user
        userdel <name> [flags] # delete a user
        ```
    -   Working with groups
        ```bash
        groupadd <group> [flags] # create a group
        groupmod <group> [flags] # edit group
        groupdel <group> [flags] # delete group
        usermod -a -G <groups> <user> # add a user to groups
        gpasswd --delete <user> <groups> # remove a user from groups
        ```
    -   System files
        ```bash
        /etc/passwd # a file containing basic information about users
        /etc/shadow # a file containing encrypted passwords
        /etc/group # a file containing basic information about groups
        /etc/gshadow # a file containing encrypted group passwords
        ```

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Managing Users, Groups and Permissions in Linux**](https://omarrrz-lounge.hashnode.dev/managing-users-groups-and-permissions-in-linux)
2. 📄 [**Linux User Groups Explained** – freeCodeCamp](https://www.freecodecamp.org/news/linux-user-groups-explained-how-to-add-a-new-group-a-new-group-member-and-change-groups/)
3. 📺 [**Linux Users and Groups** – YouTube](https://youtu.be/b-9j2jiCOEA)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Permissions

    <p align="center"><img src="./files/linux/chmod_eng.png" alt="chmod"/></p>

    In Linux, it is possible to share privileges between users, limit access to unwanted files or features, control available actions for services, and much more. In Linux, there are only three kinds of rights - read, write and execute - and three categories of users to which they can be applied - file owner, file group and everyone else.

    -   Basic commands for working with rights
        ```bash
        chown <user> <file> # changes the owner and/or group for the specified files
        chmod <rights> <file> # changes access rights to files and directories
        chgrp <group> <file> # allows users to change groups
        ```
    -   Extended rights [SUID and GUID](https://en.wikipedia.org/wiki/Setuid), [sticky bit](https://en.wikipedia.org/wiki/Sticky_bit)
    -   [ACL (Access control list)](https://en.wikipedia.org/wiki/Access-control_list)
        > An advanced subsystem for managing access rights.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**An Introduction to Linux Permissions** – Digital Ocean](https://www.digitalocean.com/community/tutorials/an-introduction-to-linux-permissions)
2. 📺 [**Understanding File & Directory Permissions** – YouTube](https://youtu.be/4e669hSjaX8)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Working with processes

    Linux processes can be described as containers in which all information about the state of a running program is stored. If a program hangs and you need to restore it, then you need the skills to manage the processes.

    -   Basic Commands
        ```bash
        ps # display a snapshot of the processes of all users
        top # real-time task manager
        <command> & # running the process in the background, (without occupying the console)
        jobs # list of processes running in the background
        fg <PID> # return the process back to the active mode by its number
        bg <PID> # start a stopped process in the background
        kill <PID> # terminate the process by PID
        killall <programm> # terminate all processes related to one program
        ```

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How to Show Process Tree in Linux**](https://linuxhandbook.com/show-process-tree/)
2. 📄 [**How To Use ps, kill, and nice to Manage Processes in Linux** – Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-use-ps-kill-and-nice-to-manage-processes-in-linux)
3. 📺 [**Linux processes, init, fork/exec, ps, kill, fg, bg, jobs** – YouTube](https://youtu.be/TJzltwv7jJs)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Working with SSH

    [SSH]() allows remote access to another computer's terminal. In the case of a personal computer, this may be needed to solve an urgent problem, and in the case of a server, it is generally the primary method of connection.

    -   Basic commands
        ```bash
        apt install openssh-server # installing SSH (out of the box almost everywhere)
        service ssh start # start SSH
        service ssh stop # stop SSH
        ssh -p <port> user@remote_host # connecting to a remote PC via SSH
        ssh-keygen -t rsa # RSA key generation for passwordless login
        ssh-copy-id -i ~/.ssh/id_rsa user@remote_host # copying a key to a remote machine
        ```

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What the hell is SSH?**](https://codingpastor.hashnode.dev/what-the-hell-is-ssh)
2. 📺 [**Learn SSH In 6 Minutes - Beginners Guide to SSH Tutorial** – YouTube](https://youtu.be/v45p_kJV9i4)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Task Scheduler

    <p align="center"><img src="./files/linux/cron_eng.png" alt="cron"/></p>

    Schedulers allow you to flexibly manage the delayed running of commands and scripts. Linux has a built-in [cron](https://en.wikipedia.org/wiki/Cron) scheduler that can be used to easily perform necessary actions at certain intervals.

    -   Main commands
        ```bash
        crontab -e # edit the crontab file of the current user
        crontab -l # output the contents of the current schedule file
        crontab -r # deleting the current schedule file
        ```
    -   Config files

        ```bash
        /etc/crontab # base config
        /etc/cron.d/ # crontab files used to manage the entire system

        # config files for automatically run programs:
        /etc/cron.daily/ # every day
        /etc/cron.weekly/ # every week
        /etc/cron.monthly/ # every month
        ```

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How to schedule and manage tasks using crontab** – dev.to](https://dev.to/shaikh/how-to-schedule-and-manage-tasks-using-crontab-20dj)
2. 📺 [**Cron Jobs For Beginners | Linux Task Scheduling** – YouTube](https://youtu.be/v952m13p-b4)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### System logs

    [Log files]() are special text files that contain all information about the operation of a computer, program, or user. They are especially useful when bugs and errors occur in the operation of a program or server. It is recommended to periodically review log files, even if nothing suspicious happens.

    -   Main log files
        ```bash
        /var/log/syslog или /var/log/messages # information about the kernel,
        # various services detected, devices, network interfaces, etc.
        /var/log/auth.log или /var/log/secure # user authorization information
        /var/log/faillog # failed login attempts
        /var/log/dmesg # information about device drivers
        /var/log/boot.log # operating system boot information
        /var/log/cron # cron task scheduler report
        ```
    -   [lnav utility](https://lnav.org/)
        > Designed for easy viewing of log files (highlighting, reading different formats, searching, etc.)
    -   Log rotation with [logrotate](https://github.com/logrotate/logrotate)
        > Allows you to configure automatic deletion (cleaning) of log files so as not to clog memory.
    -   [Demon journald](https://manpages.ubuntu.com/manpages/bionic/man1/journalctl.1.html)
        > Collects data from all available sources and stores it in binary format for convenient and dynamic control

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**Linux Crash Course - Understanding Logging** – YouTube](https://youtu.be/6uP_f_z3CbM)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Linux problems

    -   Problems with commands in the terminal
        > Occur due to erroneous actions of the user. Often associated with typos, lack of rights, incorrectly specified options, etc.
    -   Driver problems
        > All free Linux drivers are built right into its kernel. Therefore, everything should work "out of the box" after installing the system (problems may occur with brand new hardware which has just been released on the market). Drivers whose source code is closed are considered proprietary and are not included in the kernel but are installed manually (like Nvidia graphics drivers).
    -   Problems with kernel
        > [Kernel panic]() can occur due to an error when mounting the root file system.
        > This is best helped by the skill of reading the logs to find problems (`dmesg` command).
    -   [Segmentation fault]()
        > Occurs when a process accesses invalid memory locations.
    -   Disk and file system problems
        > Can occur due to lack of space.

<details>
    <summary>🔗 <b>References</b></summary>
    
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## General knowledge

-   ### Numeral systems

    [Numeral system](https://en.wikipedia.org/wiki/Numeral_system) is a set of symbols and rules for denoting numbers. In computer science, it is customary to distinguish four main number systems: binary, octal, decimal, and hexadecimal. It is connected, first of all, with their use in various branches of programming.

    -   [Binary number](https://en.wikipedia.org/wiki/Binary_number)
        > The most important system for computing technology. Its use is justified by the fact that the logic of the processor is based on only two states (on/off, open/closed, high/low, true/false, yes/no, high/low).

    <p align="center"><img src="./files/common/binary.png" alt="Binary"/></p>

    -   [Octal](https://en.wikipedia.org/wiki/Octal)
        > It is used e.g. in Linux systems to grant access rights.

    <p align="center"><img src="./files/common/octal.png" alt="Octal"/></p>

    -   [Decimal](https://en.wikipedia.org/wiki/Decimal)
        > A system that is easy to understand for most people.
    -   [Hexadecimal]()
        > The letters A, B, C, D, E, F are additionally used for recording. It is widely used in low-level programming and computer documentation because the minimum addressable memory unit is an 8-bit byte, the values of which are conveniently written in two hexadecimal digits.

    <p align="center"><img src="./files/common/hex.png" alt="Hex"/></p>

    -   Translation between different number systems
        > You can try [online converter](https://cheatsnake.github.io/NSConverter/) for a better understanding.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**Number Systems Introduction - Decimal, Binary, Octal & Hexadecimal** – YouTube](https://youtu.be/FFDMzbrEXaE)
1. 📄 [**Number System in Maths** – GeeksGorGeeks](https://www.geeksforgeeks.org/number-system-in-maths/)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Logical connective

    [Logical connective](https://en.wikipedia.org/wiki/Logical_connective) are widely used in programming to check various conditions. The result of a logical expression is always _truth_ or _false_.

    <p align="center"><img src="./files/common/logic_eng.png" alt="Logic"/></p>

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**Logical Operators − Negation, Conjunction & Disjunction** – YouTube](https://youtu.be/6kYngPvoGxU)
2. 📺 [**Logical Operators − Exclusive OR** – YouTube](https://youtu.be/m2mf6I3g2-c)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Data structures

    [Data structures](https://en.wikipedia.org/wiki/Data_structure) are containers in which data is stored according to certain rules. Depending on these rules, the data structure will be effective in some tasks and ineffective in others. Therefore, it is necessary to understand when and where to use this or that structure.

    -   [Array](<https://en.wikipedia.org/wiki/Array_(data_structure)>)
        > A data structure that allows you to store data of the same type, where each element is assigned a different sequence number.

    <p align="center"><img src="./files/common/array_eng.png" alt="Array"/></p>

    -   [Linked list](https://en.wikipedia.org/wiki/Linked_list)
        > A data structure where all elements, in addition to the data, contain references to the next and/or previous element. There are 3 varieties:
        >
        > -   A [singly linked list](https://en.wikipedia.org/wiki/Linked_list#Singly_linked_list) is a list where each element stores a link to the next element only (one direction).
        > -   A [doubly linked list](https://en.wikipedia.org/wiki/Doubly_linked_list) is a list where the items contain links to both the next item and the previous one (two directions).
        > -   A [circular linked list](https://en.wikipedia.org/wiki/Linked_list#Circular_linked_list) is a kind of bilaterally linked list, where the last element of the ring list contains a pointer to the first and the first to the last.

    <p align="center"><img src="./files/common/linked-list.png" alt="Linked list"/></p>

    -   [Stack](<https://en.wikipedia.org/wiki/Stack_(abstract_data_type)>)
        > Structure where data storage works on the principle of _last in - first out_ (LIFO).

    <p align="center"><img src="./files/common/stack_eng.png" alt="Stack"/></p>

    -   [Queue](<https://en.wikipedia.org/wiki/Queue_(abstract_data_type)>)
        > Structure where data storage is based on the principle of _first in - first out_ (FIFO).

    <p align="center"><img src="./files/common/queue.gif" alt="Queue"/></p>

    -   [Hash table](https://en.wikipedia.org/wiki/Hash_table)
        > In other words, it is an associative array. Here, each of the elements is accessed with a corresponding key value, which is calculated using [hash function](https://en.wikipedia.org/wiki/Hash_function) according to a certain algorithm.

    <p align="center"><img src="./files/common/hash-table_eng.png" alt="Hash Table"/></p>

    -   [Tree](<https://en.wikipedia.org/wiki/Tree_(data_structure)>)
        > Structure with a hierarchical model, as a set of related elements, usually not ordered in any way.

    <p align="center"><img src="./files/common/tree.png" alt="Tree"/></p>

    -   [Heap](<https://en.wikipedia.org/wiki/Heap_(data_structure)>)
        > Similar to the tree, but in the heap, the items with the largest key is the root node (max-heap). But it may be the other way around, then it is a min heap.

    <p align="center"><img src="./files/common/heap_eng.png" alt="Heap"/></p>

    -   [Graph](<https://en.wikipedia.org/wiki/Graph_(discrete_mathematics)>)
        > A structure that is designed to work with a large number of links.

    <p align="center"><img src="./files/common/graph_eng.png" alt="Graph"/></p>

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**CS50 2022 - Lecture about Data Structures** – YouTube](https://youtu.be/X8h4dq9Hzq8)
2. 📺 [**Data Structures Easy to Advanced Course** – YouTube](https://youtu.be/RBSGKlAvoiM)
3. 📄 [**Free courses to learn data structures and algorithms in depth** – freeCodeCamp](https://www.freecodecamp.org/news/these-are-the-best-free-courses-to-learn-data-structures-and-algorithms-in-depth-4d52f0d6b35a/)
4. 📄 [**Data Structures: collection of topics** – GeeksForGeeks](https://www.geeksforgeeks.org/data-structures/)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Basic algorithms

    [Algorithms](https://de.wikipedia.org/wiki/Algorithmus) refer to sets of sequential instructions (steps) that lead to the solution of a given problem. Throughout human history, a huge number of algorithms have been invented to solve certain problems in the most efficient way. Accordingly, the correct choice of algorithms in programming will allow you to create the fastest and most resource-intensive solutions.

    > There is a very good book on algorithms for beginners – [Grokking algorithms](https://edu.anarcho-copy.org/Algorithm/grokking-algorithms-illustrated-programmers-curious.pdf). You can start [learning a programming language](#programming-language) in parallel with it.

    -   [Binary search](https://en.wikipedia.org/wiki/Binary_search_algorithm)
        > Maximum efficient search algorithm for sorted lists.
    -   [Selection sort](https://en.wikipedia.org/wiki/Selection_sort)
        > At each step of the algorithm, the minimum element is searched for and then swapped with the current iteration element.
    -   [Recursion](https://en.wikipedia.org/wiki/Recursion)
        > When a function can call itself and so on to infinity. On the one hand, recursion-based solutions look very elegant, but on the other hand, this approach quickly leads to stack overflow and is recommended to be avoided.
    -   [Bubble sort](https://en.wikipedia.org/wiki/Bubble_sort)
        > At each iteration neighboring elements are sequentially compared, and if the order of the pair is wrong, the elements are swapped.
    -   [Quicksort](https://en.wikipedia.org/wiki/Quicksort)
        > Improved bubble sorting method.
    -   [Breadth-first search](https://en.wikipedia.org/wiki/Breadth-first_search)
        > Allows to find all shortest paths from a given vertex of the graph.
    -   [Dijkstra's algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)
        > Finds the shortest paths between all vertices of a graph and their length.
    -   [Greedy algorithm](https://en.wikipedia.org/wiki/Greedy_algorithm)
        > An algorithm that at each step makes locally the best choice in the hope that the final solution will be optimal.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Code for the book Grokking Algorithms** – GitHub](https://github.com/egonSchiele/grokking_algorithms)
2. 📺 [**Algorithms and Data Structures Tutorial** – YouTube](https://youtu.be/8hly31xKli0)
3. 📄 [**Largest open-source algorithm library**](https://the-algorithms.com/)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Algorithm complexity

    <p align="center"><img src="./files/common/BigO_eng.png" alt="BigO"/></p>

    In the world of programming there is a special unit of measure **Big O** (or O-notation). It describes how the complexity of an algorithm increases with the amount of input data. **Big O** estimates how many actions (steps/iterations) it takes to execute the algorithm, while always showing the worst case scenario.

    -   Varieties of algorithm complexity
        > -   Constant - O(1) <br>
        > -   Linear - O(n) <br>
        > -   Logarithmic - O(log n) <br>
        > -   Linearimetric - O(n \* log n) <br>
        > -   Quadratic - O(n^2) <br>
        > -   Stepwise - О(2^n) <br>
        > -   Factorical - O(!n) <br>

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Big O Algorithm Complexity cheatsheet**](https://www.bigocheatsheet.com/)
2. 📺 [**Big O Notation - Full Course** – YouTube](https://youtu.be/Mo4vesaut8g)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Data storage formats

    Different file formats can be used to store and transfer data over the network. Text files are human-readable, so they are used for configuration files, for example. But transferring data in text formats over the network is not always rational, because they weigh more than their corresponding binary files.

    -   Text formats

        -   [JSON (JavaScript Object Notation)](https://en.wikipedia.org/wiki/JSON)
            > Represents an object in which data is stored as key-value pairs.
        -   [YAML (Yet Another Markup Language)](https://en.wikipedia.org/wiki/YAML)
            > The format is close to markup languages like HTML. Minimalist, because it has no opening or closing tags. Easy to edit.
        -   [XML (eXtensible Markup Language)](https://en.wikipedia.org/wiki/XML)
            > The format is closer to HTML. Here the data is wrapped in opening and closing tags.

    -   Binary formats
        -   [Message Pack](https://msgpack.org/)
            > Binary analog of JSON. Allows you to pack data 15-20% more efficiently.
        -   [BSON (Binary JavaScript Object Notation)](https://en.wikipedia.org/wiki/BSON)
            > It is a superset of JSON, including additionally regular expressions, binary data and dates.
        -   [ProtoBuf (Protocol Buffers)](https://en.wikipedia.org/wiki/Protocol_Buffers)
            > Binary alternative to XML text format. Simpler, more compact and faster.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**Data Formats: XML, JSON, and YAML** – YouTube](https://youtu.be/JQO-x8rzNVI)
2. 📺 [**Serialization formats: JSON and Protobuf** – YouTube](https://youtu.be/uGYZn6xk-hA)
3. 📺 [**Protocol Buffers Crash Course** – YouTube](https://youtu.be/46O73On0gyI)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Text encodings

    Computers work only with numbers, or more precisely, only with 0 and 1. It is already clear how to convert numbers from different number systems to binary. But you can't do that with text. That's why special tables called [encodings](https://en.wikipedia.org/wiki/Character_encoding) were invented, in which text characters are assigned numeric equivalents.

    -   [ASCII (American standard code for information interchange)](https://en.wikipedia.org/wiki/ASCII)
        > The simplest encoding created specifically for the American alphabet. Consists of 128 characters.
    -   [Unicode](https://en.wikipedia.org/wiki/Unicode)
        > This is an international character table that, in addition to the English alphabet, contains the alphabets of almost all countries. It can hold more than a million different characters (the table is currently incomplete).
    -   [UTF-8](https://en.wikipedia.org/wiki/UTF-8)
        > Unicode is a variable-length encoding that can be used to represent any unicode character.
    -   [UTF-16](https://en.wikipedia.org/wiki/UTF-16)
        > Its main difference from UTF-8 is that its structural unit is not one but two bytes. That is, in UTF-16 any Unicode character can be encoded by either two or four bytes.

<details>
    <summary>🔗 <b>References</b></summary>
    
1. 📺 [**Unicode, in friendly terms: ASCII, UTF-8 and more** – YouTube](https://youtu.be/ut74oHojxqo)
2. 📺 [**Unicode Encoding! UTF-32, UCS-2, UTF-16, & UTF-8!** – YouTube](https://youtu.be/uTJoJtNYcaQ)
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Programming Language

At this stage you have to choose one programming language to study. There is plenty of information on various languages in the Internet (books, courses, thematic sites, etc.), so you should have no problem finding information.

> Below is a list of specific languages that [personally, in my opinion](https://github.com/cheatsnake) are good for backend development (⚠️ may not agree with the opinions of others, including those more competent in this matter).

-   [Python](<https://en.wikipedia.org/wiki/Python_(programming_language)>)
    > A very popular language with a wide range of applications. Easy to learn due to its simple syntax.
-   [JavaScript](https://en.wikipedia.org/wiki/JavaScript)
    > No less popular and practically the only language for full-fledged Web-development. Thanks to the platform [Node.js](https://en.wikipedia.org/wiki/Node.js) last few years is gaining popularity in the field of backend development as well.
-   [Go](<https://en.wikipedia.org/wiki/Go_(programming_language)>)
    > A language created internally by Google. It was created specifically for high-load server development. Minimalistic syntax, high performance and rich standard library.
-   [Kotlin](<https://en.wikipedia.org/wiki/Kotlin_(programming_language)>)
    > A kind of modern version of [Java](<https://en.wikipedia.org/wiki/Java_(programming_language)>). Simpler and more concise syntax, better type-safety, built-in tools for multithreading. One of the best choices for Android development.

Find a good book or online tutorial in English at [this repository](https://github.com/EbookFoundation/free-programming-books/blob/main/books/free-programming-books-langs.md). There is a large collection for different languages and frameworks.

Look for a special [awesome repository](https://github.com/sindresorhus/awesome#programming-languages) - a resource that contains a huge number of useful links to materials for your language (libraries, cheat sheets, blogs and other various resources).

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Classification of programming languages

    There are many programming languages. They are all created for a reason. Some languages may be very specific and used only for certain purposes. Also, different languages may use different approaches to writing programs. They may even run differently on a computer. In general, there are many different [classifications](https://en.wikipedia.org/wiki/Category:Programming_language_classification), which would be useful to understand.

    -   Depending on language level
        -   [Low level languages](https://en.wikipedia.org/wiki/Low-level_programming_language)
            > As close to machine code as possible, complex to write, but as productive as possible. As a rule, it provides access to all of the computer's resources.
        -   [High-level languages](https://en.wikipedia.org/wiki/High-level_programming_language)
            > They have a fairly high level of abstraction, which makes them easy to write and easy to use. As a rule, they are safer because they do not provide access to all of the computer's resources.
    -   [Compiled, interpreted and embedded languages](https://en.wikipedia.org/wiki/Programming_language#Implementation)
        -   [Compilation](https://en.wikipedia.org/wiki/Compiler)
            > Allows you to convert the source code of a program to an executable file.
        -   [Interpretation](<https://en.wikipedia.org/wiki/Interpreter_(computing)>)
            > The source code of a program is translated and immediately executed (interpreted) by a special interpreter program.
    -   [Depending on the programming paradigm](https://en.wikipedia.org/wiki/Programming_paradigm)
        -   [The Imperative Paradigm](https://en.wikipedia.org/wiki/Imperative_programming)
        -   [The Declarative Paradigm](https://en.wikipedia.org/wiki/Declarative_programming)
        -   [Metaprogramming](https://en.wikipedia.org/wiki/Metaprogramming)

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Classifying Programming Languages**](https://cs.lmu.edu/~ray/notes/pltypes/)
2. 📺 [**What are the Types of Programming Languages?** – YouTube](https://youtu.be/Mo4vesaut8g)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Language Basics

    By foundations are meant some fundamental ideas present in every language.

    -   Variables and constants
    -   Data types
        > Strings, integers, floats, booleans, etc.
    -   Operators
        > Mathematical operators, comparison operators, bitwise operators.
    -   Functions
        > Working with arguments and return values. <br>
        > Understanding the scope of variables.
    -   Flow control
        > Cycles for, conditions if else, switch-case statement.
    -   Data structures
        > Arrays, objects, classes, etc.
    -   Standard Library
        > This refers to the language's built-in capabilities to manipulate strings, numbers, arrays, etc.
    -   [Regular expressions](./files/programming-language/regex-cheatsheet.md)
        > A powerful tool for working with strings. Be sure to familiarize yourself with it in your language, at least on a basic level.
    -   Package Manager
        > Sooner or later, there will be a desire to use third-party libraries.

    After mastering the minimal base for writing the simplest programs, there is not much point in continuing to learn without having specific goals (without practice, everything will be forgotten). You need to think of/find something that you would like to create yourself (a game, a chatbot, a website, a mobile/desktop application, whatever). For inspiration, check out these repositories: [Build your own x](https://github.com/codecrafters-io/build-your-own-x) and [Project based learning](https://github.com/practical-tutorials/project-based-learning).

    At this point, the most productive part of learning begins: You just look for all kinds of information to implement your project. Your best friends are Google, YouTube, and Stack Overflow.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Free Interactive Python Tutorial**](https://www.learnpython.org/)
2. 📺 [**Python Tutorial for Beginners** – YouTube](https://youtu.be/8124kv-632k)
3. 📄 [**Python cheatsheet** – Learn X in Y minutes](https://learnxinyminutes.com/docs/python/)
4. 📄 [**Python cheatsheet** – quickref.me](https://quickref.me/python)
5. 📄 [**Free Interactive JavaScript Tutorial**](https://www.learn-js.org/)
6. 📺 [**JavaScript Programming - Full Course** – YouTube](https://youtu.be/jS4aFq5-91M)
7. 📄 [**The Modern JavaScript Tutorial**](https://javascript.info/)
8. 📄 [**JavaScript cheatsheet** – Learn X in Y minutes](https://learnxinyminutes.com/docs/javascript/)
9. 📄 [**JavaScript cheatsheet** – quickref.me](https://quickref.me/javascript)
10. 📄 [**Go Tour – learn most important features of the language**](https://go.dev/tour/list)
11. 📺 [**Learn Go Programming - Golang Tutorial for Beginners** – YouTube](https://youtu.be/YS4e4q9oBaU)
12. 📄 [**Go cheatsheet** – Learn X in Y minutes](https://learnxinyminutes.com/docs/go/)
13. 📄 [**Go cheatsheet** – quickref.me](https://quickref.me/golang)
14. 📄 [**Learn Go by Examples**](https://golangbyexample.com/)
15. 📄 [**Get started with Kotlin**](https://kotlinlang.org/docs/getting-started.html)
16. 📺 [**Learn Kotlin Programming – Full Course for Beginners** – YouTube](https://youtu.be/EExSSotojVI)
17. 📄 [**Kotlin cheatsheet** – Learn X in Y minutes](https://learnxinyminutes.com/docs/kotlin/)
18. 📄 [**Kotlin cheatsheet** – devhints.io](https://devhints.io/kotlin)
19. 📄 [**Learn Regex step by step, from zero to advanced**](https://regexlearn.com)
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Server development

    -   Creating and running a local HTTP server
    -   Handing out static files
        > Hosting HTML pages, pictures, PDFs, etc.
    -   Routing
        > Creation of endpoints (URLs) which will call the appropriate handler on the server when accessed.
    -   Processing requests
        > As a rule, HTTP handlers have a special object which receives all information about user request (headers, method, request body, full url with parameters, etc.)
    -   Processing responses
        > Sending an appropriate message to a received request (HTTP status and code, response body, headers, etc.)
    -   Error handling
        > You should always consider cases where the user could send invalid data, the database failed to execute the operation, or an unexpected error occurred in the application, so that the server does not crash but responds with an error message.
    -   Sending requests
        > Often, within one application, you will need to access another application over the network. That's why it's important to be able to send HTTP requests using the built-in features of the language.
    -   [Template processor](https://en.wikipedia.org/wiki/Template_processor)
        > Is a special module that uses a more convenient syntax to generate HTML based on dynamic data.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Learn Django – Python-based web framework**](https://www.djangoproject.com/start/)
2. 📺 [**Python Django 7 Hour Course** – YouTube](https://youtu.be/PtQiiknWUcI)
3. 📄 [**A curated list of awesome things related to Django** – GitHub](https://github.com/wsvincent/awesome-django)
4. 📺 [**Build servers in pure Node.js** – YouTube](https://youtu.be/_1xa8Bsho6A)
5. 📄 [**Learn Express – web framework for Node.js**](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs)
6. 📺 [**Express.js 2022 Course** – YouTube](https://youtube.com/playlist?list=PL_cUvD4qzbkwp6pxx27pqgohrsP8v1Wj2)
7. 📄 [**A curated list of awesome Express.js resources** – GitHub](https://github.com/rajikaimal/awesome-express)
8. 📄 [**How to build servers in Go**](https://eli.thegreenplace.net/2021/rest-servers-in-go-part-1-standard-library/)
9. 📺 [**Golang server development course** – YouTube](https://youtube.com/playlist?list=PLzUGFf4GhXBL4GHXVcMMvzgtO8-WEJIoY)
10. 📄 [**List of libraries for working with network in Go** – GitHub](https://github.com/avelino/awesome-go#networking)
11. 📄 [**Learn Ktor – web framework for Kotlin**](https://ktor.io/learn/)
12. 📺 [**Ktor - REST API Tutorials** – YouTube](https://youtube.com/playlist?list=PLFmuMD2V4CkyR0Pa42Cqu5mIhH17uG8nN)
13. 📄 [**Kotlin for server side**](https://kotlinlang.org/docs/server-overview.html)
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Multithreading

    Computers today have processors with several physical and virtual cores, and if we take into account server machines, their number can reach up to hundreds. All of these available resources would be good to use to the fullest, for maximum application performance. That is why modern server development cannot do without implementing [multithreading](<https://en.wikipedia.org/wiki/Multithreading_(computer_architecture)>) and [paralleling](https://en.wikipedia.org/wiki/Parallel_computing).

    -   [Race conditions & data races](https://en.wikipedia.org/wiki/Race_condition)
        > The main problems that arise when using multithreading.
    -   Creating processes
    -   Creating threads
    -   [Corutines](https://en.wikipedia.org/wiki/Coroutine)
        > Lightweight code execution threads organized on top of operating system threads. They can exist as separate libraries or be already built into the kernel.
    -   [Linearizability](https://en.wikipedia.org/wiki/Linearizability)
        > Operations that are performed completely, or not performed at all.
    -   Lockouts
        > Using [semaphores](<https://en.wikipedia.org/wiki/Semaphore_(programming)>) and [mutexes](<https://en.wikipedia.org/wiki/Lock_(computer_science)>) to synchronize data.

<details></details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**Multithreading Code - Computerphile** – YouTube](https://youtu.be/7ENFeb-J75k)
2. 📺 [**Threading vs multiprocessing in Python** – YouTube](https://youtu.be/AZnGRKFUU0c)
3. 📺 [**When is NodeJS Single-Threaded and when is it Multi-Threaded?** – YouTube](https://youtu.be/gMtchRodC2I)
4. 📺 [**How to use Multithreading with "worker threads" in Node.js?** – YouTube](https://youtu.be/MuwJJrfIfsU)
5. 📺 [**Concurrency in Go** – YouTube](https://youtube.com/playlist?list=PLsc-VaxfZl4do3Etp_xQ0aQBoC-x5BIgJ)
6. 📺 [**Kotlin coroutines** – YouTube](https://youtube.com/playlist?list=PLQkwcJG4YTCQcFEPuYGuv54nYai_lwil_)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Advanced Topics

    -   [Garbage collector](<https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)>)
        > A process that has made high-level languages very popular - it allows the programmer not to worry about memory allocation and freeing. Be sure to familiarize yourself with the subtleties of its operation in your own language.
    -   [Debuger](https://en.wikipedia.org/wiki/Debugging)
        > Handy tool for analyzing program code and identifying errors.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**How to Use a Debugger - Debugger Tutorial** – YouTube](https://youtu.be/7qZBwhSlfOo)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Code quality

    During these long years that programming has existed, a huge amount of code, programs and entire systems have been written. And as a consequence, there have been all sorts of problems in the development of all this. First of all they were related to scaling, support, and the entry threshold for new developers. Clever people, of course, did not sit still and started to solve these problems, thus creating so-called patterns/principles/approaches for writing high-quality code.

    By learning programming best practices, you will not only make things better for yourself, but also for others, because other developers will be working with your code.

    -   [DRY (Don't Repeat Yourself)](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
    -   [KISS (Keep It Simple, Stupid)](https://en.wikipedia.org/wiki/KISS_principle)
    -   [YAGNI (You Aren't Gonna Need It)](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)
    -   [SOLID](https://en.wikipedia.org/wiki/SOLID)
        -   [**S**ingle Responsibility](https://en.wikipedia.org/wiki/Single-responsibility_principle)
        -   [**O**pen–Closed](https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle)
        -   [**L**iskov Substitution](https://en.wikipedia.org/wiki/Liskov_substitution_principle)
        -   [**I**nterface Segregation](https://en.wikipedia.org/wiki/Interface_segregation_principle)
        -   [**D**ependency Inversion](https://en.wikipedia.org/wiki/Dependency_inversion_principle)
    -   [GRASP (General Responsibility Assignment Software Patterns)](<https://en.wikipedia.org/wiki/GRASP_(object-oriented_design)>)

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**KISS, SOLID, YAGNI And Other Fun Acronyms**](https://blog.bitsrc.io/kiss-solid-yagni-and-other-fun-acronyms-b5d207530335)
2. 📺 [**Uncle Bob SOLID principles** – YouTube](https://youtu.be/zHiWqnTWsn4)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Databases

[Databases (DB)](https://en.wikipedia.org/wiki/Database) – a set of data that are organized according to certain rules (for example, a library is a database for books).

[Database management system (DBMS)](https://en.wikipedia.org/wiki/Database#Database_management_system) is a software that allows you to create a database and manipulate it conveniently (perform various operations on the data). An example of a DBMS is a librarian. He can easily and efficiently work with the books in the library: give out requested books, take them back, add new ones, etc.

-   ### Database classification

    Databases can differ significantly from each other and therefore have different areas of application. To understand what database is suitable for this or that task, it is necessary to understand the classification.

    -   [Relational DB](https://en.wikipedia.org/wiki/Relational_model)
        > These are repositories where data is organized as a set of tables (with rows and columns). Interactions between data are organized on the basis of links between these tables. This type of database provides fast and efficient access to structured information.
    -   [Object-oriented DB](https://en.wikipedia.org/wiki/Object_database)
        > Here data is represented as objects with a set of attributes and methods. Suitable for cases where you need high-performance processing of data with a complex structure.
    -   [Distributed DB](https://en.wikipedia.org/wiki/Distributed_database)
        > Composed of several parts located on different computers (servers). Such databases may completely exclude information duplication, or completely duplicate it in each distributed copy (for example, as [Blockchain](https://en.wikipedia.org/wiki/Blockchain)).
    -   [NoSQL](https://en.wikipedia.org/wiki/NoSQL)
        > Stores and processes unstructured or weakly structured data. This type of database is subdivided into subtypes:
        >
        > -   [Key–value DB](https://en.wikipedia.org/wiki/Key%E2%80%93value_database) <br>
        > -   [Column family DB](https://en.wikipedia.org/wiki/Column_family) <br>
        > -   [Document-oriented DB](https://en.wikipedia.org/wiki/Document-oriented_database) (store data as a hierarchy of documents) <br>
        > -   [Graph DB](https://en.wikipedia.org/wiki/Graph_database) (are used for data with a large number of links)

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Comparing database types: how database types evolved to meet different needs**](https://www.prisma.io/dataguide/intro/comparing-database-types)
2. 📄 [**SQL vs NoSQL Database – A Complete Comparison**](https://backendless.com/sql-vs-nosql-database-a-complete-comparison/)
3. 📺 [**7 Database Paradigms** – YouTube](https://youtu.be/W2Z7fbCLSTw)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Relational database

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### MongoDB

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Redis

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### ACID Requirements

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Designing databases

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## API development

-   ### REST API

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### GraphQL

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### WebSockets

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### RPC and gRPC

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### WebRTC

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Software

-   ### Git version control system

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Docker

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Postman/Insomnia

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Web servers

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Message brokers

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Security

-   ### Web application vulnerabilities

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Environment variables

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Hashing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Authentication and authorization

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### SSL/TLS

<details>
    <summary>🔗 <b>References</b></summary>

</details>
 
<div align="right"><a href="#top">Contents ⬆️</a></div>

## Testing

-   ### Unit Tests

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Integration tests

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### E2E tests

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Load testing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Regression testing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Optimization

-   ### Profiling

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Caching

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Load balancing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Documentation

-   ### Markdown

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Documentation inside code
<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### API Documentation

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Static generators

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Building architecture

-   ### Architectural templates

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Design patterns

<details>
    <summary>🔗 <b>References</b></summary>
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Monolithic and microservice architecture

<details>
    <summary>🔗 <b>References</b></summary>
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Horizontal and vertical scaling

<details>
    <summary>🔗 <b>References</b></summary>
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Additional and similar resources

-   [Backend Developer Roadmap: Learn to become a modern backend developer](https://roadmap.sh/backend)
-   [Hussein Nasser – YouTube channel about networking](https://www.youtube.com/c/HusseinNasser-software-engineering)
-   [CS50 2022 – Harvard University's course about programming](https://youtube.com/playlist?list=PLeLzIg9tqA3LQW-RiFA8zJUBcTKqUVLMU)
-   [A curated and opinionated list of resources (English & Russian) for Backend developers](https://github.com/zhashkevych/awesome-backend)

<div align="center">Made with &#9829;</div>
<div align="center"><a href="https://github.com/cheatsnake/backend-cheats/blob/master/LICENSE">LICENSE</a> 2022</div>
