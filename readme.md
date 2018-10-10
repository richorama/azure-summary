# Table of Contents

* [Compute](#compute)
* [Networking](#networking)
* [Storage](#storage)
* [Web](#web)
* [Mobile](#mobile)
* [Containers](#containers)
* [Databases](#databases)
* [Analytics](#analytics)
* [AI & Machine Learning](#ai--machine-learning)
* [Internet of Things](#internet-of-things)
* [Integration](#integration)
* [Identity](#identity)
* [Security](#security)
* [DevOps](#devops)
* [Management and Governance](#management-and-governance)
* [Media](#media)
* [Microsoft Azure Stack](#microsoft-azure-stack)

## Useful Links

Service Limits: https://docs.microsoft.com/en-gb/azure/azure-subscription-service-limits

Locate your nearest Data Center: https://richorama.github.io/AzureSpeedTest2/

# COMPUTE
## Virtual Machines

IaaS Virtual machines with Windows or Linux.

https://azure.microsoft.com/en-gb/services/virtual-machines/

## SAP HANA on Azure Large Instances

SAP HANA is an in-memory, column-oriented, relational database management system developed and marketed by SAP SE.

The SAP HANA on Azure Large Instances solution builds on non-shared host/server bare-metal hardware that is assigned to you. The server hardware is embedded in larger stamps that contain compute/server, networking, and storage infrastructure.

Units are available up to 480 Intel CPU cores and up to 24 TB of memory.

https://docs.microsoft.com/en-us/azure/virtual-machines/workloads/sap/hana-overview-architecture

## Cloud Services

Part of the original Azure offering, Cloud Services are a PaaS with the ability to control the whole virtual machine.

You can install your own software on VMs that use Azure Cloud Services, and you can access them remotely.

Software has to be packaged prior to deployment.

Two flavours are available, Web Roles and Worker Roles. The former has IIS installed and supports web applications.

Supports .NET, Java, Node.js, PHP, Python & Ruby.

https://docs.microsoft.com/en-us/azure/cloud-services/cloud-services-choose-me

## Virtual Machine Scale Sets

Azure virtual machine scale sets let you create and manage a group of identical, load balanced VMs. 

The number of VM instances can automatically increase or decrease in response to demand or a defined schedule. 

https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/overview

## Functions

Azure Functions is a serverless solution for easily running small pieces of code, or "functions," in the cloud.

Supports C#, F#, Node.js, Java, or PHP

Pay only for the time your code runs, Azure will scale as needed. 

https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview

## Batch

Run large-scale parallel and high-performance computing (HPC) applications efficiently.

Manage batch jobs using Powershell, Azure CLI, .NET, Java, Node.js, Python and the Azure Portal.

Azure Batch creates and manages a pool of VMs, installs the applications you want to run, and schedules jobs to run on the nodes. 

You pay for the underlying resources consumed, such as the virtual machines, storage, and networking.

Container workloads can be used.

https://docs.microsoft.com/en-us/azure/batch/

## Service Fabric

Azure Service Fabric is a distributed systems platform that makes it easy to package, deploy, and manage scalable and reliable microservices and containers.

https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-overview

# NETWORKING

## Virtual Network

Azure Virtual Network enables many types of Azure resources, such as Azure Virtual Machines (VM), to securely communicate with each other, the internet, and on-premises networks.

https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview

## Load Balancer

Load Balancer distributes new inbound flows that arrive on the Load Balancer's frontend to backend pool instances, according to rules and health probes.

* Load-balance incoming internet traffic to your VMs. This configuration is known as a Public Load Balancer.
* Load-balance traffic across VMs inside a virtual network. You can also reach a Load Balancer front end from an on-premises network in a hybrid scenario. Both scenarios use a configuration that is known as an Internal Load Balancer.
* Port forward traffic to a specific port on specific VMs with inbound network address translation (NAT) rules.
* Provide outbound connectivity for VMs inside your virtual network by using a public Load Balancer.

https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview

## Application Gateway

A OSI layer 7 web traffic load balancer that enables you to route traffic to your web applications.

URL Path Based Routing allows you to route traffic to back-end server pools based on URL Paths of the request (i.e. /video/* gets routed to a paticular server pool).

Redirection support:
* Global redirection from one port to another port on the application gateway. This enables HTTP to HTTPS redirection on a site.
* Path-based redirection. This type of redirection enables HTTP to HTTPS redirection only on a specific site area, for example a shopping cart area denoted by /cart/*.
* Redirect to an external site.

Multiple-site hosting enables you to configure more than one web site on the same Application Gateway instance. This feature allows you to configure a more efficient topology for your deployments by adding up to 20 web sites to one application gateway. 

Session affinity (sticky sessions)

SSL termination

Firewall

Websocket HTTP/2 support

https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-introduction

## VPN Gateway

A VPN gateway is a specific type of virtual network gateway that is used to send encrypted traffic between an Azure virtual network and an on-premises location over the public Internet. 

You can also use a VPN gateway to send encrypted traffic between Azure virtual networks over the Microsoft network. 

https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways

## Azure DNS

Azure DNS is a hosting service for DNS domains, providing name resolution using Microsoft Azure infrastructure.

https://docs.microsoft.com/en-us/azure/dns/dns-overview

## Content Delivery Network

A content delivery network (CDN) is a distributed network of servers that can efficiently deliver web content to users. CDNs store cached content on edge servers in point-of-presence (POP) locations that are close to end users, to minimize latency.

Supports caching of a Storage account, Cloud Service, Web App or a custom origin.

https://docs.microsoft.com/en-us/azure/cdn/cdn-overview

## Traffic Manager

Azure Traffic Manager is a DNS-based traffic load balancer that enables you to distribute traffic optimally to services across global Azure regions.

https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-overview

## ExpressRoute

ExpressRoute lets you extend your on-premises networks into the Microsoft cloud over a private connection facilitated by a connectivity provider. 

https://docs.microsoft.com/en-us/azure/expressroute/expressroute-introduction

## Network Watcher

Azure Network Watcher provides tools to monitor, diagnose, view metrics, and enable or disable logs for resources in an Azure virtual network.

https://docs.microsoft.com/en-us/azure/network-watcher/network-watcher-monitoring-overview

## Azure Firewall

Azure Firewall can limit outbound HTTP/S traffic to a specified list of fully qualified domain names (FQDN) including wild cards. 

You can centrally create allow or deny network filtering rules by source and destination IP address, port, and protocol. Azure Firewall is fully stateful, so it can distinguish legitimate packets for different types of connections.

FQDN tags

Outbound SNAT support

Inbound DNAT support

https://docs.microsoft.com/en-us/azure/firewall/overview

## Azure Front Door Service

Front Door works at Layer 7 or HTTP/HTTPS layer and uses anycast protocol with split TCP and Microsoft's global network for improving global connectivity. You can route requests to the fastest and most available application backend. 

An application backend is any Internet-facing service hosted inside or outside of Azure. 

https://docs.microsoft.com/en-us/azure/frontdoor/front-door-overview

## Virtual WAN

Azure Virtual WAN is a networking service that provides optimized and automated branch-to-branch connectivity through Azure.

https://docs.microsoft.com/en-us/azure/virtual-wan/virtual-wan-about

# STORAGE
## Storage

Azure Storage is a Microsoft-managed service providing cloud storage that is highly available, secure, durable, scalable, and redundant. Azure Storage includes Azure Blobs (objects), Azure Data Lake Storage Gen2, Azure Files, Azure Queues, and Azure Tables. 

Client libraries are available for Powershell, Azure CLI, .NET, Java, Python and Node.js.

Encryption at reset and client-side encryption are supported.

Replication options:

* __Locally-redundant storage (LRS)__: A simple, low-cost replication strategy. Data is replicated within a single storage scale unit.
* __Zone-redundant storage (ZRS)__: Replication for high availability and durability. Data is replicated synchronously across three availability zones.
* __Geo-redundant storage (GRS)__: Cross-regional replication to protect against region-wide unavailability.
* __Read-access geo-redundant storage (RA-GRS)__: Cross-regional replication with read access to the replica

Azure Blob storage is Microsoft's object storage solution for the cloud. Blob storage is optimized for storing massive amounts of unstructured data, such as text or binary data.

Azure Files enables you to set up highly available network file shares that can be accessed by using the standard Server Message Block (SMB) protocol. That means that multiple VMs can share the same files with both read and write access. You can also read the files using the REST interface or the storage client libraries.

The Azure Queue service is used to store and retrieve messages. Queue messages can be up to 64 KB in size, and a queue can contain millions of messages. Queues are generally used to store lists of messages to be processed asynchronously.

Azure Table storage is a service that stores structured NoSQL data in the cloud, providing a key/attribute store with a schemaless design.

Azure Storage also includes managed and unmanaged disk capabilities used by virtual machines. 

https://docs.microsoft.com/en-us/azure/storage/

## StorSimple

A hybrid cloud strorage system, allowing infrequently files stored on a on-prem SAN to be archived and backed up to the cloud. 

# WEB
## App Service

Web Apps is a PaaS for web based applications. It offers auto-scaling and high availability, supports both Windows and Linux, and enables automated deployments.

Supports .NET, .NET Core, Node.js, PHP, Java, static sites & containers.

Deploy using FTP, Git, Azure DevOps, GitHub, BitBucket, Dropbox, OneDrive.

An app runs in an App Service plan. An App Service plan defines a set of compute resources for a web app to run. These compute resources are analogous to the server farm in conventional web hosting. One or more apps can be configured to run on the same computing resources (or in the same App Service plan).

* __Shared compute__: Free and Shared, the two base tiers, runs an app on the same Azure VM as other App Service apps, including apps of other customers. These tiers allocate CPU quotas to each app that runs on the shared resources, and the resources cannot scale out.
* __Dedicated compute__: The Basic, Standard, Premium, and PremiumV2 tiers run apps on dedicated Azure VMs. Only apps in the same App Service plan share the same compute resources. The higher the tier, the more VM instances are available to you for scale-out.
* __Isolated__: This tier runs dedicated Azure VMs on dedicated Azure Virtual Networks, which provides network isolation on top of compute isolation to your apps. It provides the maximum scale-out capabilities.
* __Consumption__: This tier is only available to function apps. It scales the functions dynamically depending on workload. For more information, see Azure Functions hosting plans comparison.

https://docs.microsoft.com/en-us/azure/app-service/

## Mobile apps

Mobile apps builds on top of Azure Apps, providing additional services:

* __Authentication and authorization__: Support for identity providers, including Azure Active Directory for enterprise authentication, plus social providers such as Facebook, Google, Twitter, and Microsoft accounts.

* __Data access__: An OData v3 data source that's linked to Azure SQL Database or an on-premises SQL server.

* __Offline sync__: The client SDKs make it easy to build robust and responsive mobile applications that operate with an offline dataset.

* __Push notifications__: The client SDKs integrate seamlessly with the registration capabilities of Azure Notification Hubs, so you can send push notifications to millions of users simultaneously.

https://docs.microsoft.com/en-us/azure/app-service-mobile/app-service-mobile-value-prop

## API Management

Used in front of your own application API to provide extra features to consumers:

* Accepts API calls and routes them to your backends.
* Verifies API keys, JWT tokens, certificates, and other credentials.
* Enforces usage quotas and rate limits.
* Transforms your API on the fly without code modifications.
* Caches backend responses where set up.
* Logs call metadata for analytics purposes.

https://docs.microsoft.com/en-us/azure/api-management/api-management-key-concepts

## Azure Search

A search-as-a-service allowing you to create a search index, and query it over REST.

Full text search and text analysis

Cognitive search (preview)

Azure Search indexes accept data from any source, provided it is submitted as a JSON data structure. 

Automatically crawl Azure SQL Database, Azure Cosmos DB, or Azure Blob storage for searchable content. 

Azure Blob indexers can perform document cracking to extract text from major file formats, including Microsoft Office, PDF, and HTML documents.

Linguistic analysis

Geo-search

Relevance

Monitoring and reporting

https://docs.microsoft.com/en-us/azure/search/search-what-is-azure-search

## Azure SignalR Service

ASP.NET SignalR is a library for ASP.NET developers that simplifies the process of adding real-time web functionality to applications.

SignalR provides an abstraction over a number of techniques used for building real-time web applications. WebSockets is the optimal transport, but other techniques like Server-Sent Events (SSE) and Long Polling are used when other options aren't available.

With Azure SignalR Service, the server-side component of ASP.NET Core SignalR is hosted in Azure. 

https://docs.microsoft.com/en-us/azure/azure-signalr/signalr-overview

# MOBILE
## Notification Hubs

Azure Notification Hubs allows you to send push notifications to any platform (iOS, Android, Windows, Kindle, Baidu, etc.) from any backend (cloud or on-premises). 

https://docs.microsoft.com/en-us/azure/notification-hubs/notification-hubs-push-notification-overview

## Visual Studio App Centre

Visual Studio App Centre will build, test, distribute, and monitor your mobile apps. It also supports push notifications.

* __Build__: Create an installable app package automatically with every push to your repository. Supports GitHub, or Git repos on Bitbucket and Azure DevOps.
* __Test__: Run your tests on more than 400 unique device configurations.
* __Distribute__: Users can install the app via email distribution lists for testing.
* __Diagnostics__: Collect crash data from all devices, prioritize them based on the number of users seeing the crash, and get the full stack traces to help you fix them.
* __Analytics__: Get information about the number of daily, weekly, and monthly users, session duration, the top devices etc...
* __Push Notifications__: Send users targeted push notifications.

https://docs.microsoft.com/en-us/appcenter/

# CONTAINERS
## Azure Kubernetes Service (AKS)

Deploy a managed Kubernetes cluster in Azure. 

https://docs.microsoft.com/en-us/azure/aks/intro-kubernetes

## Azure Container Service

Deploy Kubernetes, DC/OS, or Docker Swarm cluster.

For Kubernetes clusters, consider the Azure Kubernetes Service.

https://docs.microsoft.com/en-us/azure/container-service/

## Container Instances

Azure Container Instances offers the fastest and simplest way to run a container in Azure, without having to provision any virtual machines and without having to adopt a higher-level service. 

https://docs.microsoft.com/en-us/azure/container-instances/container-instances-overview

## Container Registry

Azure Container Registry is a managed Docker registry service based on the open-source Docker Registry 2.0.

Create and maintain Azure container registries to store and manage your private Docker container images.

https://docs.microsoft.com/en-us/azure/container-registry/container-registry-intro

# DATABASES
## SQL Data Warehouse

SQL Data Warehouse is a cloud-based Enterprise Data Warehouse (EDW) that leverages Massively Parallel Processing (MPP) to quickly run complex queries across petabytes of data.

https://docs.microsoft.com/en-us/azure/sql-data-warehouse/sql-data-warehouse-overview-what-is

## Azure Cosmos DB

Azure Cosmos DB is a globally distributed, multi-model database service that supports document, key-value, wide-column, and graph databases.

It supports multiple client APIs:
* SQL
* MongoDB
* Gremlin
* Table Storage
* Cassandra

https://docs.microsoft.com/en-us/azure/cosmos-db/

## Azure SQL Database

SQL Database is a general-purpose relational database managed service.

Feature comparison between SQL Database and SQL Server: https://docs.microsoft.com/en-us/azure/sql-database/sql-database-features

https://docs.microsoft.com/en-us/azure/sql-database/sql-database-technical-overview

## Azure Database for MySQL

A relational database service in the Microsoft cloud based on the MySQL Community Edition database engine. 

https://docs.microsoft.com/en-us/azure/mysql/overview

## Azure Database for MariaDB

A relational database service in the Microsoft cloud based on the MariaDB community edition database engine. 

https://docs.microsoft.com/en-us/azure/mariadb/overview

## Azure Database for PostgreSQL

Azure Database for PostgreSQL is a relational database service in the Microsoft cloud built for developers based on the community version of open-source PostgreSQL database engine.

https://docs.microsoft.com/en-us/azure/postgresql/overview

## Redis Cache

Redis is an open-source in-memory data structure project implementing a distributed, in-memory key-value database. Redis supports data structures, such as strings, lists, maps, sets, sorted sets, hyperloglogs, bitmaps and spatial indexes.

Azure Redis Cache is Redis as a Service. Clustering and persistence are offered by a premium tier.

https://docs.microsoft.com/en-us/azure/redis-cache/cache-overview

## SQL Server Stretch Database

Stretch Database migrates your cold data stored in SQL Server 2016 (Windows only) transparently and securely to the the cloud.

https://docs.microsoft.com/en-us/sql/sql-server/stretch-database/stretch-database?view=sql-server-2017

# ANALYTICS
## Azure Databricks

An Apache Spark-based analytics platform with these features:

* __Spark SQL and DataFrames__: Spark SQL is the Spark module for working with structured data. A DataFrame is a distributed collection of data organized into named columns. It is conceptually equivalent to a table in a relational database or a data frame in R/Python.

* __Streaming__: Real-time data processing and analysis for analytical and interactive applications. Integrates with HDFS, Flume, and Kafka.

* __MLib__: Machine Learning library consisting of common learning algorithms and utilities, including classification, regression, clustering, collaborative filtering, dimensionality reduction, as well as underlying optimization primitives.

* __GraphX__: Graphs and graph computation for a broad scope of use cases from cognitive analytics to data exploration.

* __Spark Core API__: Includes support for R, SQL, Python, Scala, and Java.

https://docs.microsoft.com/en-us/azure/azure-databricks/what-is-azure-databricks

## HDInsight

HDInsight is a cloud distribution of the Hadoop components from the Hortonworks Data Platform (HDP). 

You can use open-source frameworks such as Hadoop, Spark, HBase, Kafka, Storm, Hive and R.

https://docs.microsoft.com/en-us/azure/hdinsight/

## Data Factory

Allows you to create and schedule data-driven workflows (called pipelines) that can ingest data from disparate data stores. 

It can process and transform the data by using compute services such as Azure HDInsight Hadoop, Spark, Azure Data Lake Analytics, and Azure Machine Learning.

You can publish output data to data stores such as Azure SQL Data Warehouse for business intelligence (BI) applications to consume.

https://docs.microsoft.com/en-us/azure/data-factory/introduction

## Stream Analytics

Azure Stream Analytics is an event-processing engine that allows you to examine high volumes of data streaming from devices. 

It supports extracting information from data streams, identifying patterns, and relationships.

You can then use these patterns to trigger other actions downstream, like alerts, feed information to a reporting tool, or store it for later use.

Stream Analytics starts with a source of streaming data that is ingested into Azure Event Hub, Azure IoT Hub or from a data store like Azure Blob Storage. 

https://docs.microsoft.com/en-us/azure/stream-analytics/stream-analytics-introduction

## Data Lake Analytics

Azure Data Lake Analytics is an on-demand analytics job service. It provisions resources for analytics on terabytes to petabytes of data.

Integrates with Visual Studio

It uses U-SQL, a query language that extends SQL with C#.

It works aganst data stored in 
* Azure Data Lake Store (for the highest performance, throughput, and parallelization)
* Blob storage
* SQL Database
* Azure Warehouse

https://docs.microsoft.com/en-us/azure/data-lake-analytics/data-lake-analytics-overview

## Event Hubs

Azure Event Hubs is a Big Data streaming platform and event ingestion service, capable of receiving and processing millions of events per second.

* __Event producers__: Any entity that sends data to an event hub. Event publishers can publish events using HTTPS or AMQP 1.0 or Apache Kafka (1.0 and above)
* __Partitions__: Each consumer only reads a specific subset, or partition, of the message stream.
* __Consumer groups__: A view (state, position, or offset) of an entire event hub. Consumer groups enable multiple consuming applications to each have a separate view of the event stream, and to read the stream independently at their own pace and with their own offsets.
* __Throughput units__: Pre-purchased units of capacity that control the throughput capacity of Event Hubs.
* __Event receivers__: Any entity that reads event data from an event hub. All Event Hubs consumers connect via the AMQP 1.0 session, and events are delivered through the session as they become available.

https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-about

## Power BI Embedded

Power BI Embedded is for independent software vendors (ISVs) and for developers who build applications for their customers. It can be used as a third-party business intelligence service that enables you to visualize application data, rather than building that service yourself. 

https://docs.microsoft.com/en-gb/power-bi/developer/azure-pbie-what-is-power-bi-embedded

## Azure Analysis Services

Analysis Services is an analytical data engine used in decision support and business analytics. It provides enterprise-grade semantic data models for business reports and client applications such as Power BI, Excel, Reporting Services reports, and other data visualization tools.

Azure Analysis Services is a hosted Analysis Services.

https://docs.microsoft.com/en-us/azure/analysis-services/analysis-services-overview

## Data Catalog

Data Catalog provides a cloud-based service into which a data source can be registered. The data remains in its existing location, but a copy of its metadata is added to Data Catalog, along with a reference to the data-source location. 

This provides a way for people within an organisation to discover a wide variety of internal data sources, such as files, databases, APIs etc...

https://docs.microsoft.com/en-us/azure/data-catalog/data-catalog-what-is-data-catalog

## Azure Data Lake Storage

Azure Data Lake Storage provides big data analytics on Azure Blob Storage. 

https://docs.microsoft.com/en-us/azure/storage/data-lake-storage/introduction

## Azure Data Explorer

A data exploration service for log and telemetry data.

Azure Data Explorer supports several ingestion methods, including connectors to common services like Event Hub, programmatic ingestion using SDKs, such as .NET and Python, and direct access to the engine for exploration purposes.

Azure Data Explorer integrates with analytics and modeling services for additional analysis and visualization of data.

Work in Azure Data Explorer generally follows this pattern:

* __Create database__: Create a cluster and then create one or more databases in that cluster.

* __Ingest data__: Load data into database tables so that you can run queries against it.

* __Query database__: Use a web app or REST API to run, queries. 

Data can be semi-structured (JSON-like nested types) and unstructured (free-text).

https://docs.microsoft.com/en-us/azure/data-explorer/data-explorer-overview

# AI + MACHINE LEARNING
## Azure Batch AI

Azure Batch AI is a managed service to help data scientists and AI researchers train and test machine learning and AI models at scale in Azure.

Batch AI has built-in support for popular open-source AI libraries and frameworks including TensorFlow, PyTorch, Chainer, and Microsoft Cognitive Toolkit (CNTK).

https://docs.microsoft.com/en-us/azure/batch-ai/overview

## Azure Bot Service

Azure Bot Service provides an integrated environment that is purpose-built for bot development, enabling you to build, connect, test, deploy, and manage intelligent bots.

Azure Bot Service leverages the Bot Builder SDK with support for C# and JavaScript. 

https://docs.microsoft.com/en-us/azure/bot-service/bot-service-overview-introduction?view=azure-bot-service-4.0

## Microsoft Genomics

Microsoft Genomics offers a cloud implementation of the Burrows-Wheeler Aligner (BWA) and the Genome Analysis Toolkit (GATK) for secondary analysis. 

https://docs.microsoft.com/en-us/azure/genomics/overview-what-is-genomics

## Machine Learning service

Azure Machine Learning service is a cloud service that you can use to develop and deploy machine learning models. 

You can track your models as you build, train, deploy, and manage them,

Azure Machine Learning Studio is a collaborative, drag-and-drop visual workspace where you can build, test, and deploy machine learning solutions without needing to write code. It uses pre-built and pre-configured machine learning algorithms and data-handling modules.

Use Machine Learning Studio when you want to experiment with machine learning models quickly and easily, and the built-in machine learning algorithms are sufficient for your solutions.

https://docs.microsoft.com/en-us/azure/machine-learning/service/overview-what-is-azure-ml

## Cognitive Services

Azure Cognitive Services are APIs, SDKs, and services available to help developers build intelligent applications without having direct AI or data science skills or knowledge.

### Vision APIs

* __Computer Vision__: Provides you with access to advanced algorithms for processing images and returning information.
* __Custom Vision Service__: Allows you to build custom image classifiers.
* __Content Moderator__: Provides monitoring for possible offensive, undesirable, and risky content.
* __Face API__: Provides access to advanced face algorithms, enabling face attribute detection and recognition.
* ___Emotion API__: Takes an image as an input and returns the confidence across a set of emotions for each face in the image.
* __Video Indexer__: Enables you to extract insights from your video.

### Speech APIs

* __Speech Service__: Adds speech-enabled features to applications.
* __Custom Speech Service__: Allows you to create customized language models and acoustic models tailored to your application and your users.
* __Bing Speech API__: Provides you with an easy way to create speech-enabled features in your applications.
* __Translator Speech__: A machine translation service.
* __Speaker Recognition API__: Provides algorithms for speaker identification and verification.

### Language APIs

* __Bing Spell Check__: Allows you to perform contextual grammar and spell checking.
* __Language Understanding LUIS__: Allows your application to understand what a person wants in their own words.
* __Linguistic Analysis__: Provides natural language processing tools that identify the structure of text.
* __Text Analytics__: Provides natural language processing over raw text for sentiment analysis, key phrase extraction and language detection.
* __Translator Text__: Provides for machine-based text translation in near real-time.
* __Web Language Model__: Natural language processing for predicting word sequencing, completions, and word breaking of strings with no spaces.

### Search APIs

* __Bing News Search__: Returns a list of news articles determined to be relevant to the user's query.
* __Bing Video Search__: Returns a list of videos determined to be relevant to the user's query.
* __Bing Web Search__: Returns a list of search results determined to be relevant to the user's query.
* __Bing Autosuggest__: Allows you to send a partial search query term to Bing and get back a list of suggested queries.
* __Bing Custom Search__: Allows you to create tailored search experiences for topics that you care about.
* __Bing Entity Search__: Returns information about entities that Bing determines are relevant to a user's query.
* __Bing Image Search__: Returns a display of images determined to be relevant to the user's query.
* __Bing Visual Search__: Returns insights about an image such as visually similar images, shopping sources for products found in the image, and related searches.

### Knowledge APIs

* __Custom Decision Service__: Helps you create intelligent systems with contextual decision making for personalizing and optimizing user experience.
* __QnA Maker__: Allows you to build a question and answer service from your semi-structured content.

https://docs.microsoft.com/en-us/azure/cognitive-services/welcome

# INTERNET OF THINGS
## IoT Hub

IoT Hub is a managed service, hosted in the cloud, that acts as a central message hub for bi-directional communication between your IoT application and the devices it manages. 

* Per-device authentication enables each device to connect securely to IoT Hub and for each device to be managed securely.
* The IoT Hub Device Provisioning Service automatically provisions devices to the right IoT hub when the device first boots up.
* Multiple authentication types support a variety of device capabilities (SaS tokens, X.509 certs, X.509 CA).
* Store, synchronize, and query device metadata and state information for all your devices.
* Set device state either per-device or based on common characteristics of devices.
* Automatically respond to a device-reported state change with message routing integration.

Supported languages on devices:

* C
* C#
* Java
* Python
* Node.js

Supported protocols: 

* HTTPS
* AMQP
* AMQP over WebSockets
* MQTT
* MQTT over WebSockets

https://docs.microsoft.com/en-us/azure/iot-hub/about-iot-hub

## IoT Central

Azure IoT Central is a fully managed SaaS solution that makes it easy to connect, monitor and manage your IoT assets.

https://docs.microsoft.com/en-us/azure/iot-central/overview-iot-central

## Time Series Insights

Time Series Insights (TSI) is built for storing, visualizing, and querying large amounts of time series data, such as that generated by IoT devices.

* Consume message from Azure IoT Hub and Azure Event Hubs. It parses JSON from messages and structures that have data in clean rows and columns. It joins metadata with telemetry and indexes your data in a columnar store.
* Data is strored for up to 400 days.
* Provides out-of-the-box visualization via TSI explorer.
* Provides a query service, both in the TSI explorer and by using APIs.

https://docs.microsoft.com/en-us/azure/time-series-insights/time-series-insights-overview

## Azure Maps

Azure Maps is a collection of geospatial services, backed by mapping data so you can provide geographic context to your applications.

It contains REST APIs for rendering maps and searching points of interest.

The APIs can also find routes to points of interest, traffic conditions, time zones, and a location from an IP address. 

Available in all countries except:

* Argentina
* China
* India
* Morocco
* Pakistan
* South Korea

https://docs.microsoft.com/en-us/azure/azure-maps/about-azure-maps

## Event Grid

Azure Event Grid is an event routing service that allows for uniform event consumption using a publish-subscribe model.

Use Azure Event Grid to react to relevant events across both Azure and non-Azure services in near-real time fashion.

Event sources:

* Azure Subscriptions (management operations)
* Container Registry
* Custom Topics
* Event Hubs
* IoT Hub
* Media Services
* Resource Groups (management operations)
* Service Bus
* Storage Blob
* Storage General-purpose v2 (GPv2)

Event handlers:

* Azure Automation
* Azure Functions
* Event Hubs
* Hybrid Connections
* Logic Apps
* Microsoft Flow
* Queue Storage
* WebHooks

https://docs.microsoft.com/en-us/azure/event-grid/overview

## Logic Apps

Azure Logic Apps is a cloud service that helps you automate and orchestrate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across enterprises or organizations.
 
There are 200+ connectors, which include services such as Azure Service Bus, Functions, Storage, SQL, Office 365, Dynamics, Salesforce, BizTalk, SAP, Oracle DB, file shares.

https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-overview

## Windows 10 IoT Core Services

Windows 10 IoT Core Services services to commercialize a device on Windows 10 IoT Core. 

OEMs have access to 10 years of support on Windows 10 IoT Core Long Term Servicing Channel (LTSC) releases along with services to manage device updates and assess device health.

Useful if you are creating a device and you control the update and maintenance of the full software image on the device.

https://docs.microsoft.com/en-us/windows-hardware/manufacture/iot/iotcoreservicesoverview

## Azure Sphere

Azure Sphere is a secured, high-level application platform with built-in communication and security features for internet-connected devices.

Azure Sphere introduces a new class of secured, connected, crossover microcontroller unit (MCU), which integrates real-time processing capabilities with the ability to run a high-level operating system.

An Azure Sphere MCU, along with its operating system and application platform, enables product manufacturers to create secured, internet-connected devices that can be updated, controlled, monitored, and maintained remotely.

https://docs.microsoft.com/en-us/azure-sphere/product-overview/what-is

# INTEGRATION
## Service Bus

Microsoft Azure Service Bus is a fully managed enterprise integration message broker. 

Queues provide point-to-point communication. Queues enable you to store messages until the receiving application is available to receive and process them.

Topics provide publish/subscribe scenarios. You can use rules and filters to define conditions that trigger optional actions, filter specified messages, and set or modify message properties.


* __Message sessions__: Message sessions enable joint and ordered handling of unbounded sequences of related messages (FIFO guarantee).
* __Auto-forwarding__: Chain a queue or subscription to another queue or topic that is part of the same namespace.
* __Dead-lettering__: A dead-letter queue (DLQ) holds messages that cannot be delivered to any receiver, or messages that cannot be processed.
* __Scheduled delivery__: You can submit messages to a queue or topic for delayed processing.
* __Message deferral__: Clients have the option to defer retrieval of the message to a later point. The message remains in the queue or subscription, but it is set aside.
* __Batching__: Client-side batching enables a queue or topic client to delay sending a message for a certain period of time. If the client sends additional messages during this time period, it transmits the messages in a single batch.
* __Transactions__: operations against a single messaging entity (queue, topic, subscription) can be grouped within the scope of a transaction.
* __Filtering and actions__: Subscribers can define which messages they want to receive from a topic.
* __Auto-delete on idle__: Enables you to specify an idle interval after which the queue is automatically deleted.
* __Duplicate detection__: The queue or topic can discard any duplicate copies of a message.
* __SAS, RBAC, and MSI__: Security protocols such as Shared Access Signatures (SAS), Role Based Access Control (RBAC) and Managed Service Identity (MSI).
* __Geo-disaster recovery__: Geo-disaster recovery enables data processing to continue operating in a different region or datacenter.
* __Security__: AMQP 1.0 and HTTP/REST protocols are supported.

https://docs.microsoft.com/en-us/azure/service-bus-messaging/service-bus-messaging-overview

## Service Bus Relay

The Azure Relay service facilitates hybrid applications by enabling you to securely expose services that reside within a corporate enterprise network to the public cloud, without having to open a firewall connection, or require intrusive changes to a corporate network infrastructure. 

* __Hybrid Connections__: Uses the open standard web sockets enabling multi-platform scenarios.

* __WCF Relays__: Uses Windows Communication Foundation (WCF) to enable remote procedure calls. WCF Relay is the legacy relay offering that many customers already use with their WCF programming models.

The relay capabilities differ from network-level integration technologies such as VPN, in that relay can be scoped to a single application endpoint on a single machine, without altering the network enviroment.

https://docs.microsoft.com/en-us/azure/service-bus-relay/relay-what-is-it

## BizTalk Services

_Microsoft Azure BizTalk Services (MABS) is being retired and replaced with Azure Logic Apps._

# IDENTITY
## Active Directory B2C

Azure Active Directory (Azure AD) B2C is an identity management service that enables you to customize and control how customers sign up, sign in, and manage their profiles when using your applications. This includes applications developed for iOS, Android, and .NET, among others. 

* Enable a customer to sign up to use your registered application
* Enable a signed-up customer to sign in and start using your application
* Enable a signed-up customer to edit their profile
* Enable multi-factor authentication in your application
* Enable the customer to sign up and sign in with specific identity providers
* Grant access from your application to APIs that you build
* Customize the look and feel of the sign-up and sign-in experience
* Manage single sign-on sessions for your application

https://docs.microsoft.com/en-us/azure/active-directory-b2c/active-directory-b2c-overview

## Active Directory Domain Services

Azure AD Domain Services provides managed domain services such as domain join, group policy, LDAP, Kerberos/NTLM authentication that are fully compatible with Windows Server Active Directory.

https://docs.microsoft.com/en-us/azure/active-directory-domain-services/active-directory-ds-overview

## Active Directory

A directory, and identity management service. 

Provides single sign-on access.

Provides Multi-Factor Authentication.

Self-service password resets.

https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-whatis

## Enterprise State Roaming

Allows Azure Active Directory (Azure AD) users to gain the ability to securely synchronize their user settings and application settings data to the cloud.

https://docs.microsoft.com/en-us/azure/active-directory/active-directory-windows-enterprise-state-roaming-overview

# SECURITY
## Azure DDoS Protection

* __Basic__: Automatically enabled as part of the Azure platform. Traffic monitoring, and real-time mitigation of common network-level attacks, provide the same defenses utilized by Microsoft’s online services.
* __Standard__: Provides additional mitigation capabilities. Protection policies are tuned through dedicated traffic monitoring and machine learning algorithms.

DDoS Protection Standard can mitigate the following types of attacks:

* __Volumetric attacks__: UDP floods, amplification floods, and other spoofed-packet flood.
* __Protocol attacks__: SYN flood attacks, reflection attacks, and other protocol attacks. 
* __Resource (application) layer attacks__: HTTP protocol violations, SQL injection, cross-site scripting, and other layer 7 attacks.

https://docs.microsoft.com/en-us/azure/virtual-network/ddos-protection-overview

## Security Center

Apply security policies across your workloads, limit your exposure to threats, and detect and respond to attacks.

https://docs.microsoft.com/en-us/azure/security-center/security-center-intro

## Key Vault

* __Secrets Management__: Securely store and control access to tokens, passwords, certificates, API keys, and other secrets
* __Key Management__: Create and control the encryption keys used to encrypt your data.
* __Certificate Management__: Provision, manage, and deploy public and private SSL/TLS certificates for use with Azure and your internal connected resources.
* __Store secrets backed by Hardware Security Modules__: Protected either by software or FIPS 140-2 Level 2 validates HSMs

https://docs.microsoft.com/en-us/azure/key-vault/key-vault-overview

## Azure Information Protection

Classify and protect documents and emails by applying labels. 

Track and control how the document is used.

Analyze data flows to gain insight into your business

Detect risky behaviors and take corrective measures, track access to documents, prevent data leakage or misuse.

https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection

## Access Control Service

_Azure Active Directory (Azure AD), will be retired on November 7, 2018_

# DEVOPS
## Azure DevOps

Azure DevOps Services provides development collaboration tools including pipelines, Git repositories, Kanban boards, and cloud-based load testing.

* __Azure Pipelines__: Manage CI/CD to deploy your code with pipelines that work with any language, platform, and cloud.

* __Azure Repos__: Use Git repositories, pull requests, and then integrate with CI/CD to build and deploy your apps.

* __Azure Boards__: Plan and track your work using interactive, highly-customizable backlogs and boards.

* __Azure Artifacts__: Share code with others across your teams or company, and support CI/CD of your apps.

* __Azure Test Plans__: Improve the overall code quality of your apps by using manual, exploratory, or load-based testing services.

https://docs.microsoft.com/en-us/azure/devops/?view=vsts

## Azure DevTest Labs

Quickly create environments in Azure while minimizing waste and controlling cost.

Set policies on your lab - such as number of virtual machines (VM) per user and number of VMs per lab

https://docs.microsoft.com/en-us/azure/lab-services/devtest-lab-overview

# MANAGEMENT AND GOVERNANCE
## Azure Site Recovery

Site Recovery helps ensure business continuity by keeping business apps and workloads running during outages. 

Site Recovery replicates workloads running on physical and virtual machines (VMs) from a primary site to a secondary location. 

The Azure Backup service keeps your data safe and recoverable by backing it up to Azure.

https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-overview

## Azure Portal

A web portal to manage your Azure resources using your browser.

https://azure.microsoft.com/en-us/features/azure-portal/

## Cloud Shell

Azure Cloud Shell is an interactive, browser-accessible shell for managing Azure resources.

https://docs.microsoft.com/en-us/azure/cloud-shell/overview

## Azure Advisor

Azure Advisor analyzes your resource configuration and usage telemetry and then recommends solutions that can help you improve the cost effectiveness, performance, high availability, and security of your Azure resources.

https://docs.microsoft.com/en-us/azure/advisor/advisor-overview

## Azure Backup

Back up (or protect) and restore your data in the Microsoft cloud. 

Azure Backup replaces your existing on-premises or off-site backup solution with a cloud-based solution.

https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup

## Azure Policy

Create, assign and, manage policies for Azure resources.

These policies enforce different rules and effects over your resources, so those resources stay compliant with your corporate standards and service level agreements.

Azure Policy does this by running evaluations of your resources and scanning for those not compliant with the policies you have created. For example, you can have a policy to allow only a certain SKU size of virtual machines in your environment.

https://docs.microsoft.com/en-us/azure/governance/policy/overview

## Azure Monitor

A solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments.

It collects:

* __Application monitoring data__: Data about the performance and functionality of the code you have written, regardless of its platform.
* __Guest OS monitoring data__: Data about the operating system on which your application is running. This could be running in Azure, another cloud, or on-premises.
* __Azure resource monitoring data__: Data about the operation of an Azure resource.
* __Azure subscription monitoring data__: Data about the operation and management of an Azure subscription, as well as data about the health and operation of Azure itself.
* __Azure tenant monitoring data__: Data about the operation of tenant-level Azure services, such as Azure Active Directory.

Log data collected by Azure Monitor is stored in Log Analytics which collects telemetry and other data from a variety of sources and provides a query language for analytics.

Azure Monitor provides an autoscale feature to respond to incidents by horizontally scaling your infrastructure.

https://docs.microsoft.com/en-us/azure/azure-monitor/overview

## Application Insights

Application Performance Management (APM) service for web developers on multiple platforms.

It supports .NET, Node.js and J2EE, applications hosted on-premises or in the cloud.

You install an instrumentation package in your application, and set up an Application Insights resource in the Microsoft Azure portal. The instrumentation monitors your app and sends telemetry data to the portal.

It can monitor:

* Request rates, response times, and failure rates
* Dependency rates, response times, and failure rates
* Exceptions
* Page views and load performance reported by your users' browsers
* AJAX calls from web pages
* Performance counters from your Windows or Linux server machines
* Host diagnostics from Docker or Azure
* Diagnostic trace logs
* Custom events and metrics that you write yourself in the client or server code

https://docs.microsoft.com/en-us/azure/application-insights/app-insights-overview

## Azure Resource Manager

Azure Resource Manager enables you to work with the resources in your solution as a group.

You can deploy, update, or delete all the resources for your solution in a single, coordinated operation.

You use a template for deployment and that template can work for different environments such as testing, staging, and production. 

Resource Manager provides security, auditing, and tagging features to help you manage your resources after deployment.

https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview

## Azure Managed Applications

Azure Managed Applications enables you to offer your cloud solutions to internal and external customers. You define the infrastructure for the solution, and the terms for ongoing management of the solution. The billing for your solution is handled through Azure billing.

https://docs.microsoft.com/en-us/azure/managed-applications/overview

## Scheduler

Azure Scheduler is being retired. To schedule jobs use Azure Logic Apps.

https://docs.microsoft.com/en-us/azure/scheduler/scheduler-intro

## Automation

* __Process automation__: Automate deploying, configuring, and managing your end to end processes by authoring runbooks graphically, in PowerShell, or Python.
* __Configuration management__: Manage your DSC resources in Azure Automation and apply configurations to virtual or physical machines from a DSC Pull Server in the Azure cloud.
* __Update management__: Update Windows and Linux systems across hybrid environments.

https://docs.microsoft.com/en-us/azure/automation/automation-intro

## Azure Blueprints

Azure Blueprints enables development teams to rapidly provision and stand up new environments knowing that they're built within organizational compliance and contain a set of built-in components -- such as networking -- to speed up development and delivery.

https://docs.microsoft.com/en-us/azure/governance/blueprints/overview

# MEDIA
## Media Services

Microsoft Azure Media Services (AMS) is an extensible cloud-based platform that enables developers to build scalable media management and delivery applications.

Media Services is based on REST APIs that enable you to securely upload, store, encode, and package video or audio content for both on-demand and live streaming delivery to various clients (for example, TV, PC, and mobile devices).

https://docs.microsoft.com/en-us/azure/media-services/

# MIGRATION
## Azure Migrate

The Azure Migrate service assesses on-premises workloads for migration to Azure. The service assesses the migration suitability of on-premises machines, performs performance-based sizing, and provides cost estimations for running on-premises machines in Azure. 

https://docs.microsoft.com/en-us/azure/migrate/migrate-overview

## Azure Database Migration Service

The Azure Database Migration Service is a fully managed service designed to enable seamless migrations from multiple database sources to Azure Data platforms with minimal downtime.

# MICROSOFT AZURE STACK
## Azure Stack

Microsoft Azure Stack is a hybrid cloud platform that lets you deliver Azure services in your datacenter. 

There are two versions:

* __Azure Stack integrated systems__: offered through a partnership of Microsoft and hardware partners. Systems range in size from 4-12 nodes, and are jointly supported by the hardware partner and Microsoft. 
* __Azure Stack Development Kit__: Intended for non-production use, ASDK is a single-node deployment of Azure Stack, that you can use to evaluate and learn about Azure Stack. You can also use ASDK as a developer environment to build apps using the APIs and tooling that's consistent with Azure.

https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-poc
