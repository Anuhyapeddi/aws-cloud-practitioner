# aws-cloud-practitioner
key concepts of AWS

Frameworks
Q. What is Cloud Adoption Framework?
Cloud adoption framework uses AWS to digitally transform and accelerate business outcomes.

Q. What are the perspectives and foundational capabilities of the cloud adoption framework?
  1.	Security – focuses on compliance and assurance. 
    •	Security – governance, security assurance, application security.
    •	Protection – infrastructure and data protection.
    •	Management – IAM, Vulnerability is managed here.
    •	Incident response.
    •	Threat Detection 
  2.	Business – Focuses on strategy and outcomes.
    •	Management – Strategy, Portfolio, Innovation, and product management.
    •	Data – Data Monetization, data science.
    •	Business Insight
  3.	Platform – Focuses on Infrastructure and Applications
    •	Architecture and Engineering – Platform and data 
    •	Continuous Integration/ Continuous Delivery (CI/CD)
    •	Modern Application Development
    •	Provisioning and Orchestration.
  4.	Operations – focuses on successful workload delivery.
    •	Management – Event (AIOps), Incident and Problem, Change and Release, Performance and capacity, patch, Availability and continuity,         Application management.
    •	Observability.
  5.	Governance - focuses on minimizing transformation-related risks and maximizing organizational benefits.
    •	Management – Program and project benefits, risk, cloud financial, application portfolio.
    •	Data – Data governance and data curation.
  6.	People – It creates a bridge between technology and business.
    •	Transformation – leadership and workforce transformation.
    •	Organization – design and alignment.
    •	Cloud fluency 
    •	Change Acceleration
    •	Culture Evolution.

Q. What are the cloud transformation domains?
  1.	Technology – which uses the cloud to migrate and modernize legacy infrastructure applications as well as data analytics platforms.
  2.	Process – it is used to digitize, automate, and optimize your business operations.
  3.	Organization – Focuses on how to reimagine how the business and teams orchestrate their efforts to create more value and meet goals.
  4.	Product – reimagining your business model by creating new products or services, and revenue models.

Q. What are the phases in the Cloud Adoption Framework?
  1.	Envision – Imaging or planning and helping to accelerate business outcomes.
  2.	Align – which focuses on identifying capability gaps across the six perspectives. Which are mentioned above. Finding any challenges         or areas of concern.
  3.	Lunch – deliver initiatives with value. Here we watch and adjust.
  4.	Scale – expanding those transformations across our environment and scaling out.

Well – Architecture Framework

Q. What are the six pillars of well- architecture framework?
  •	Security – includes things like the principle of least privilege, securing data at rest and transit.
  •	Cost optimization – Maintaining costs in the cloud, like the right size and implementing lifecycles.
  •	Performance efficiency – using computing resources efficiently, including topics like maximizing resource usage and trade-offs.
  •	Operational excellence – creating applications that successfully support your workloads, like event management and designing telemetry.
  •	Reliability – when a system breaks down, how much time it would take to recover (able to recover quickly). Like disaster recovery and network topology.
  •	Sustainability – energy efficiency and consumption which includes region selection and aligning infrastructure to match demand so that waste is limited.

Q. What are the general design principles?
  •	Stop guessing your capacity needs – autoscaling.
  •	Test systems at the production scale – Create a complete testing environment to stimulate your actual workload, and don’t forget to decommission it when you finish your testing.
  •	Consider Evolutionary Architectures – Allow your architecture to evolve as the needs of the workload grow and shrink.
  •	Automate with architectural experimentation in mind - Automation can save time and money while implementing a faster way to create and replicate your workloads. Disaster recovery and reduced impacts of any incidents.
  •	Drive architecture using data - Reiteration of collecting data.
  •	Improve through game days – game days help to simulate events so that your team can be ready for the real deal. Cutting back on time, perfecting processes, and finding faults and performance 

Q. What are the EC2 instance types?
  •	General purpose instance type – balances compute, memory, and networking resources
  •	Compute-optimized instance – high-performance processors.
  •	Memory-optimized instance – high-performance databases
  •	Accelerated computing instances – floating-point number calculations, graphics processing, and data pattern matching.
  •	Storage optimized instances – data warehousing applications

Security, Compliance, and Governance
-----------------------------------------------------------------------------------------------------------------------------------------
Database Services
Q. How networking is done in AWS?
  1.	Direct connect. 
  2.	VPC (Virtual Private Cloud)
  There are two types of VPC. 
  a.	Site-to-site vpc – data transfer from local system to AWS cloud 
  b.	Client vpc - data transfer from local system to anywhere in the world.

Q. What are Databases in aws?
  There are 4 types of databases:
  1.	Relational database – RDS.
  2.	Non-relational database – DynamoDB.
  3.	In-memory database (memorydb) – Amazon Elastic Cache, Amazon. MemoryDB for Redis; rather than storing the data in hard disk, it stores the data in RAM.
  4.	Graph database - Amazon's Neptune.

Q. Database migration tools?
Database Migration Service (DMS) - Used to migrate your on-premises database to aws cloud, or ec2 database to RDS.

Example:
Your Oracle database -> AWS RDS for oracle.

Schema Conversion Tool (SCT) - Converts one database schema to another.

Example:
Your Oracle database -> AWS aurora for MySQL.

MySQL -> RDS for MySQL
Sql server -> Aurora for PostgreSQL 

Development, Messaging, and Deployment Technology and Services
-----------------------------------------------------------------------------------------------------------------------------------------
Q. What is continuous Integration (CI)?
Continuous Integration (CI) in AWS refers to the practice of automatically building and testing code changes whenever developers make updates to a shared code repository. AWS provides various services and tools that support CI practices, such as AWS CodePipeline, AWS CodeBuild, and AWS CodeCommit.

Q. What are the benefits of continuous Integration/ continuous Deployment?
  •	Automation is good – fast, scalable, repeatable.
  •	No manual effort – slow, error-prone, inconsistent.
  •	Small changes applied frequently – catch bugs when they are small and simple to fix.

Q. What is continuous deployment (CD)?
Continuous Deployment (CD) in AWS is an extension of Continuous Integration (CI) where code changes that pass automated tests are automatically deployed to production environments. This means that whenever developers make changes to the codebase, those changes are automatically pushed to the production environment without manual intervention.

Q. AWS development tools?
  Codecommit
    •	it’s like a private git repository in the cloud. 
    •	It is the place to store source code, binary, images, and libraries. 
    •	It receives updates from multiple places from multiple developers so that it helps to manage, collaborate, and track code changes.
    •	Also maintains the version history.
  Codebuild 
    •	It is a fully managed build and test service. 
    •	Runs the set of commands that you define, to compile code, run tests and produce the artifacts that are ready to deploy.
    •	It can refer to the code, which is stored in the code commit repo, and use the code to build the deployable artifacts.
  Codedeploy 
    •	It is an automated deployment service.
    •	It automatically deploys the code in ec2 instance, on-premises, lambda.
    •	Avoid downtime and avoid risks by manual processes.
  Codepipeline 
    •	Codecommit -> codebuild -> codedeploy -> ec2 instance

Q. What is cloud9?
Cloud9 is an integrated development environment (IDE) that you can use inside of your browser.
That means you can write, run, and debug the code, without need to install anything in your local machines.

Q. What is codeartifact?
  •	An artifact repository makes it easy for the developers to find the right version of the code.
  •	Artifact is called documentation, complied applications, deployable packages, and library.
  •	Supports third-party or in-house developed artifacts.
  •	It is used for developers to find approved packages to the public.

Q. Decoupling application components
  Tight coupling 
    •	Components are dependent on each other. 
    •	If one fails another component will not work
  Loose coupling
    •	Components are not dependent.
    •	If one fails, it will not affect the other.

Q. What are the integration services in AWS?
  Queues -> SQS
  Notifications ->SNS
  Events -> Eventbridge

Q. What is SNS?
  •	Simple Notification Service
  •	Type of messages -> SMS text messages and emails
  •	Used the Pub-sub model, to publish the messages to the subscribers.

Q. What is SQS?
  •	Simple Queue Service 
  •	It is a temporary repository for messages that are waiting for processes.
  •	Messages wait in the queue until the consumer is ready to process them.
  •	It is a pull-based service.

Q. What are the types of SQS?
  Standard
    •	It is the default queue type.
    •	The messages are delivered at least once. 
    •	It mostly maintains order, but sometimes the order gets changed.
    •	Sometimes it has duplicates.
  FIFO
    •	First in first out.
    •	Strictly follows the order.
    •	No duplicates.

Q. What are short-polling and long-polling in SQS?
  Short polling 
    •	It will respond immediately, even if the queue is empty.
    •	You need to still pay for empty responses.
  Long polling
    •	Queue is polled periodically.
    •	It will respond Whenever the message appears in the queue, or long poll times out.
    •	It is cost cost-efficient way.

Q. What is SES?
  •	Simple Email Service
  •	It sends rich formatted HTML emails. 
  •	Always send emails in bulk. 

Q. What is the difference between SNS and SES?
SNS sends SMS text messages and plain emails to consumers. Whereas SES sends the rich formatted HTML emails to the consumers.

Q. what is EventBridge?
  •	It uses the event-driven architecture.
  •	It is simply a change in state.
  •	Can handle scheduled events, which run on the schedule. 
  •	If we schedule run once an hour, it runs once an hour.


Example:
For example, let's say you have an application that uploads files to an S3 bucket. You can configure S3 to send an event to EventBridge whenever a file is uploaded. Then, you can set up a rule in EventBridge to trigger a Lambda function whenever such an event occurs. This Lambda function can process the uploaded file, maybe by resizing images or extracting text, and then store the result in another S3 bucket or send it to another service.

In this example, EventBridge acts as the glue between the S3 bucket and the Lambda function, allowing you to easily create event-driven architectures without managing complex integrations.

Q. What is a step function?
  •	It is serverless. 
  •	It automatically triggers and tracks each step.
  •	It logs each step so that it can keep track of where the step went wrong.

Example:
seeing product -> hold product -> billing.

In each step it uses lambda.
The output of one step is the input of the next step.

Q. What is an X-ray?
  •	Provides the end-to-end view of the requests throughout your applications.
  •	It is a tool to analyze and debug distributed applications.
  •	Troubleshoot the root cause of the performance issues and errors.
  •	Allows you to visualize your application's underlying components.

Migration and Transfer Technology and Services
-----------------------------------------------------------------------------------------------------------------------------------------
Q. snowball family?
Snowball family is used for data transfer solutions. From physical to aws cloud. 

  Snowball 
    •	Can hold 10 TB or more of data.
  Snowball Edge
    •	Can hold 10 TB or more of data and need some computation process.
  Snowmobile 
    •	Shipping container full of disked towed by truck.
    •	10 pb or more.
  Snowcone 
    •	Small and portable, can hold up to 14 TB. 
    •	Mostly used for military purposes.

Q. What is the AWS Transfer family?
  •	It is used to transfer files from third party to AWS storage.
  •	Business-to-business file transfer protocol uses like SFTP, AS2, FTPS and FTP.
  •	It uses SFTP put for storing files in storage.
  •	It uses SFTP get for retrieving files from storage.

Partner -> SFTP put -> aws storage. (to store the info)
Partner -> SFTP get -> aws storage. (to get the info)

Q. What is DataSync?
  •	It is used to transfer a large amount of data to AWS storage.
  •	Data is encrypted.

Examples:
Your datacenter -> encrypted -> s3
Other cloud provides -> encrypted -> EFS.
Aws storage services -> encrypted -> aws storage services.

Q. What is an application discovery service?
  •	Used to migrate a bunch of applications or databases to AWS.
  •	Discovery tool gathers data about your existing setup. Data is collected and sent over the AWS.
  •	It is encrypted.
  •	It is stored in the migration hub.

Applications
/databases   -> application discovery service -> migration hub 

Q. How the data is collected in the Application Discovery service?
  •	By installing the application discovery service agent on your virtual machines or physical servers.
  •	Agent gathers the data and sends it to the application discovery service.
  •	We can also use an agentless collector; it is only used for VM ware.
  •	Agentless collector is installed in VMware appliance.
  •	It’s running on a separate virtual appliance instead of being an agent.


Agent 
Installed on 
Application -----> collected data ------> app discovery service.

Q. What is an application migration service?
  •	It is used to migrate applications to AWS.
  •	It automatically converts the source servers to run natively on AWS.
  •	It also performs the test before migrating to AWS.

Q. How the applications are migrated to AWS using the application migrating service?
  •	It is done by installing an aws replication agent.
  •	Application migration service performs the continuous replication from the source servers to the destinated servers.
  •	Traffic is encrypted.
  •	It is free to use for up to 90 days.

Installing replication agent 
On our server -------------> continuous replication ----------> aws.

Q. What is Migration Hub?
  •	It is the central location for managing the migration of applications and data into AWS.
  •	Enable access, plan, track, and migrate to AWS.
  •	It is used to integrate other services like application discovery service, application migration service, and database migration service.

Artificial Intelligence, Machine Learning, and Analytics Technology and Services
-----------------------------------------------------------------------------------------------------------------------------------------
Q. What is redshift?
  •	It is a data warehouse service.
  •	Used to store large amounts of data.
  •	It stores the data in petabytes(PB)
  •	Used for reporting and analyzing. Majorly used for business
  intelligence.
  •	Used for OLAP (online analytics processing)

Q. What is redshift serverless?
  •	No infrastructure to manage.

Q. What is kinesis?
  •	It is the service that collects and analyzes the streaming data.
  •	Allows you to build custom applications.

Q. What is a kinesis stream?
Stream data and videos which allows you to create custom applications.

Kinesis data stream
  •	process the streaming data.
  •	It takes the produced data and stores it in shards.
  •	Shards are data records with unique sequence numbers.
  •	Kinesis stream is made up of one or more shards.
  •	It stores data 24/7 and 365 retentions.
  •	If want to do anything with data, we can provide them to the database.
  •	consumer like ec2 instance or lambda.
  •	After the computation is done, they can send to databases like dynamo db, s3, emr, and redshift.

Producer -----> kinesis stream -----> consumer -----> database.

Mobile/laptop/ec2 -> shards in kinesis stream -> ec2/ lambda -> db.

Kinesis video stream – process the videos into aws for storage.

Q. What is kinesis data firehose?
  •	It captures, transforms, and loads data to AWS storage. It is used to make analyses like BI visualization.
  •	When the data is produced it runs in kinesis firehose. If we want to store the data. We should database.
  •	No shards and no retentions. Optionally we can perform lambda.
  •	No consumers, it directly stores data in databases like s3, and OpenSearch.

Producer -----> kinesis firehose -----> database -----> warehouse.

Mobile/ec2/iot --> kinesis firehose opt lambda --> s3 --> redshift.



Q. What is the main difference between kinesis stream and kinesis firehose?
Kinesis firehoses transform and load data in the database. Whereas kinesis will directly provide to consumers.

Q. What is Amazon Athena?
  •	Uses standard SQL queries.
  •	It is serverless.
  •	It is used for querying log files and generating reports from s3.
  •	It is an interactive query.

Q. What is Amazon Glue?
  •	Discovery, categorize, and transform the data. It is used to prepare your data for analytics and machine learning.
  •	It cleans data, removes duplicates, enriches the data, and then transforms to a database for analytic.
  •	Catalogs your data, which category the data according to their type and keeps the metadata. So that the processed data is used for analytics and machine learning.

Database -----> glue ------> Database 
Database -----> glue ------> catalog (to the specific data)

Q. Steps performed by glue?
  •	Performs ETL (extract, transform, load)
  •	Extract data from source like s3, lambda, kinesis.
  •	Transform data. Like cleaning, deleting duplicates, and joining multiple data sets.
  •	Load data into rds, redshift, s3, or Athena.

Q. What is AWS data exchange?
  •	It is the service that allows you to securely exchange data between third parties on a subscription basis.
  •	They provide the data in data product format.
  •	The format can be anything that can be stored in s3. Like csv, parquet, or image files.

Q. What does Elastic Map Reduce (EMR)?
  •	It is the big data platform. It deals with a large amount of data.
  •	Large-scale parallel processing.
  •	It deals with data in petabytes.

Q. What kind of data does Elastic Map Reduce (EMR) support?
  •	Structural data – financial transaction data.
  •	Semi Structural data – text, documentation.
  •	Unstructured data – application logs, click-stream data.

Q. What is Amazon OpenSearch?
OpenSearch is a software tool that helps you search and analyze large amounts of data quickly. It can be used to search through documents, logs, and other types of data to find specific information or patterns. It's often used in applications like search engines, log analysis, and data visualization.

Q. Why OpenSearch is better than Elastic Search?
Deploying and administering your own elastic cluster can be a time-consuming and complex process. Where the OpenSearch service comes in.

Q. What is Managed streaming for Apache Kafka?
  •	It is the service that collects and analyzes the streaming data.
  •	It same as kinesis but the main difference is it uses Apache Kafka.
  •	The users who want to use Apache Kafka but don’t want to manage the server.

Producer -----> Apache Kafka -----> consumer
Stock price data ----> Apache Kafka <----- data consumer.

Q. What is Quick Sight?
  •	Business analytic service that makes you make better decisions on your data.
  •	It can connect to AWS and on-premises.
  •	Visualize your data, like a bar graph, line graph or plot graph.

Many businesses are storing large amounts of data. Even more amount of data is produced. Among this large amount of data. How can you find which data is beneficial to you? So here comes Quick Sight which takes all your data performs some methods and gives you insights about your data. It gives you a bar graph, line graph, and plot graph.

Business data ----> quick sight -----> business decisions.

Q. What is Amazon Segamaker?
  •	Fully managed machine learning service. It helps to import and prepare data.
  •	Let’s build your model.
  •	Train your model with optimized infrastructure.
  •	Deploy your model.

Import data --> built model --> train model --> deploy model.

Q. What is Amazon Kendra?
Intelligent search service that uses natural language processing to return specific answers to search questions from your data.

  •	Kendra first indexes your documents. Indexes store the contents of your data. 
  •	After the index is created. You can question Kendra using NLP and will provide the answers using the data index.

Your data (s3, rds) -> indexes, Kendra -> answer from indexes.

Q. What is lex?
  •	Conversational chatbots.
  •	Uses nlp.

Q. What is Polly?
  •	Converts text to speech.
  •	Uses deep learning.

Q. What does amazon comprehend do?
  •	It uses NLP and ml algorithms to process data.
  •	It is used for sentimental analysis – customer opinion.
  •	Discovery of the key phrases, topics, and languages.
  •	Intelligent search – intent and context instead of keywords.

Q. What is an extract, transcribe and translate?
All 3 use machine learning algorithms.

  Textract - extract information from documents.
    •	It can process all kind of data like images, tables, and pdfs.
    •	Can also extract data from handwritten or printed.
    •	Automated ID processing.
    •	Analyzing invoices.
  
  Transcribe – speech-to-text conversion.
    •	It can deal with streamed data, or you can upload audio file like mp3 files.
    •	It is used for subtitles or automatically creating meeting notes.
  
  Translate – convert to another language.

Q. what is rekognition?
  •	Image and video analysis 
  •	Content moderation – to identify harmful and offensive images.
  •	Identity verification – e.g. Celebrities.
  •	Identify objects in images.

Auditing, Monitoring, Logging, and Additional Technology and Services
-----------------------------------------------------------------------------------------------------------------------------------------
Q. What is cloud watch?
CloudWatch is a monitoring and management service provided by Amazon Web Services (AWS). It helps you keep track of your AWS resources and applications by collecting and tracking metrics, monitoring log files, setting alarms, and automatically reacting to changes in your AWS resources. 

In simpler terms, CloudWatch acts like a set of eyes and ears for your AWS services, letting you know if something goes wrong or if there are opportunities to improve performance. For example, it can tell you if your server is running out of memory or if your website is receiving more traffic than usual.

To use this, you need to install the cloud watch agent on the ec2 instance. It also provides a dashboard.

Q. What is cloud trail? 
CloudTrail is another service provided by Amazon Web Services (AWS), but instead of monitoring your resources like CloudWatch, CloudTrail monitors and logs all actions taken on your AWS account. 

It's like having a recording of everything that happens in your account, such as who accessed it, what actions they performed, and when they did it. This information can be useful for security, auditing, and troubleshooting purposes. 

For example, if someone accidentally deletes an important file, you can use CloudTrail to see who did it and when, so you can restore the file and prevent it from happening again.

Monitors the API calls.
Track actions.

Q. What is a tag?
  •	It is used to sort and visualize cloud resources based on the category you decide.
  •	Grouping resources.
  •	Tag is the key: value pair.

Q. Define systems manager.
  •	It is used to organize your resources not only on the AWS cloud but also on-premises.
  •	There is also a parameter store, where you can securely store your passwords, database string, and license keys.

Q. Define the AWS Health dashboard.
  •	Checks the health of the resources in all regions.
  •	You can monitor by AWS health dashboard on the AWS console and 
  •	Another way to monitor your resources is by AWS Health API, here you can customize your dashboard.

Q. Define Trusted Advisor.
  •	Can advise on performance. 
  •	Cost optimization.
  •	Fault tolerance.
  •	Service limits.
  •	Security. 
  •	Operational excellence.

Q. What are the free trusted advisor checks?
  •	Do you have any open security groups?
  •	Are you using IAM users?
  •	Does your MFA is enabled in your account?
  •	Are you getting close to your service limits?
  •	Do you have any public RDS snapshots?
  •	Do you have any public ec2 volume snapshots?
  •	Do your s3 buckets have open access? 

Q. What is aws config?
  •	Pre-defined recommendations or you can set custom rules.
  •	Detects defective resources and sends alerts to administrators.

Q. What is an Audit manager?
  •	Centralize audit data from aws config and security services.
  •	You can know the root causes of the defective resources and make reports.
  •	Pre-defined frameworks like HIPPA, NIST cyber security 

Config, 
security hub -> audit manager + pre-defined frameworks -> reports.

Q. Rather than aws Config and aws audit manager. Are there any other tools that will audit?
Yes, well-architecture tool.

Q. What does Amazon Connect do?
  •	Cloud-based contact center.
  •	Allows you to create a call center in the cloud, this can be distributed call by agents, cases, and managers all over the globe.
  •	Then your manager and agents around the globe, can log into your Amazon Connect application and manage their work there.

Q. What is Amazon workspace?
  •	Provision of remote desktops for dispersed employees.
  •	Create a directory of users and give them access to the virtual desktops.

 Allocate users ---------------------> remote desktops.


Q. What is amazon AppStream?
  •	Converts applications to SaaS (software as a service) for employees or end users.
  •	Host and manage the application in the cloud, they can be accessed by the web browser.
  •	Package your application, load it into appstream, connect users, and your application is accessed by the web browser. 
  •	Here you do not need to scale or provision any resource. 

Package your application -> load into appstream -> connect users -> application is accessed by web browser. 

Security, Compliance, and Governance

Q. What is IAM (Identity Access Management)?
  •	When you attach IAM policies to users, groups, and roles. They are known as identity-based policies. 
  •	They give granular permissions.
  •	If possible, use IAM roles because they automatically rotate the access key. 

Q. What are the additional tools in IAM?
  IAM access Analyzer
    •	This identifies and alerts you, which users have external access to resources.
    •	Validate IAM policies.
    •	Generate IAM policy based on your usage.
  IAM policy simulator
    •	Test yourself before applying to users or groups.

Q. What is federated Identity?
  •	You want your users to access AWS resources. You can do it by creating IAM users like giving a unique username and password. Or it can use an already existing authentication directory.
  •	The process of using the existing authentication directory called federal identity, where your user can log in and verify the identity.

Q. What is the IAM Identity Center?
  •	IAM Identity Center is the service for Federal Identity.
  •	It is a more secure way to give access to resources than creating IAM users. 
  •	When you are giving access through IAM Identity Center and Identity Federal you are using IAM roles.
  •	When the users sign on using IAM roles, they temporarily access the resource.

Users -> identity center and identity federal -> access to resource.

Q. What is AWS directory service?
  •	IAM Identity Center cannot directly connect to the Microsoft authentication center. It uses aws directory service.
  •	It is used to connect the AWS ecosystem with an existing Microsoft authentication center.

Q. What is web federated Identity?
  •	You want your users to access your application. You can set your own authentication rules. Or you can use third-party identifier.
  •	Here AWS provides you with the web identity provider, which verifies the user identity.

Q. What is Amazon Cognito?
  •	Amazon Cognito service for web identity provider.
  •	Example login with Google, amazon, and Apple.

Q. What is aws security token service (STS)?
  •	Giving them a temporary access. Like read-only access for third-party audit.

Q. What is encryption at rest?
encryption at rest – Encryption at rest means protecting your data in place.

Methods for encryption at rest:
Server-side encryption
  •	s3 is the server-side encryption. 

Amazon Macie
  •	It is another way to keep data safe in s3.
  •	It uses the machine learning algorithms. 
  •	It scans the s3 bucket and identifies any sensitive data and PII (Personal Identity Information) is exists.

Key management service 
  •	KMS is used for encrypting the EBS volumes and RDS. 
  •	You cannot encrypt the existing rds. For that, you need to create the copy of the rds and make kms for the rds copy.

Q. What is encryption at transit?
encryption at transit - Encryption at transit means protecting your data while moving.

Methods for encryption at transit:
VPC (Virtual private cloud)
  •	All traffic within the VPN is encrypted.

Certificate manager
  •	Transferring data on HTTP is not safe. Instead, you should use https.
  •	Because https uses TLS (transport layer security) protocol
  •	Certificate manager is the service that helps you to automatically renew public or private TLS certificates.

Q. What other kinds of data should be kept secret?
Parameter store
  •	Parameter store can securely store passwords, database string, and other reference.
  •	It gives the programmatic access.
  •	Imagine, you have an ec2 instance and want to access a database. You can keep those database credentials on the parameter store. Your ec2 instance only accesses it if they have the necessary IAM role.

Systems manager
  •	It’s the same as the parameter store but more advanced.
  •	If you want to give access to the ec2 instance but don’t want to live your secrets for long. A systems manager is the best option.
  •	Allows you to rotate your secrets.

Q. What is an AWS firewall manager?
AWS Firewall Manager is a security management service that allows you to centrally configure and manage firewall rules across your accounts and applications in AWS Organizations.

Q. What are the types of AWS firewall managers?
  AWS network firewall 
    •	AWS Network Firewalls go beyond the NACLs and security groups by allowing you to define the complex rules to inspect traffic coming into VPC.
  
  AWS WAF (Web application Firewall)
    •	It protects from sql injections.
  
  AWS shield
    •	It protects from DDoS (Distributed Denial of Service) Attack.
    •	Shield advanced gives you 24/7 protection.

Q. What is a Security Hub?
  •	It supports a bunch of security and configuration services.

Q. What are the 4 security events?
  AWS Trusted Advisor
    •	Suggestions on Performance, security, fault tolerance, service limits, cost optimization, and operational excellence.
  
  Amazon GuardDuty
    •	Tracks activity logs and finds malicious behavior.
    •	Using machine learning algorithms
    •	It detects threats. 
  
  Amazon Detective 
    •	Investing in the security events that have already happened.
    •	Helps you to find the cause and the extent of the event.
  
  Amazon Inspector
    •	It continuously scans your workloads to detect vulnerabilities and network exposure.
    •	It also alerts you.

Q. What is AWS Organization?
  •	It is used to organize all your AWS accounts. 
  •	Used of consolidated billing.
  •	You can use config rules for detecting non-compliant resources across your entire AWS organization.
  •	We can also use a service control policy to prevent certain actions across your organization.

Q. What is Artifact?
  •	Where you can download and compliance.
  
Pricing, Billing, and Support
-----------------------------------------------------------------------------------------------------------------------------------------
Q. What are the ways to optimize the cost?
  Auto Scaling 
  Reserved Instance 
    •	Standard Reserved Instance 
    •	Convertible Reserved Instance 
    •	Scheduled Reserved Instance 
  Spot Instance 
  Compute optimizer 
    •	Compute optimizer is the way to get recommendations of your cost.
    •	It uses CloudWatch logs to analyze and gives you recommendations. On how to right-size your instances.
    •	It uses machine learning algorithms.
  On-demand Instances 
    •	Lambda 
    •	AWS fargate – it is used for containerized workloads like Kubernetes and ECS.

Q. What are the different s3 storage?
  Storage class 
    •	S3 Standard
    •	S3 Standard IA
    •	S3 one zone IA
    •	S3 Express Zone 
    •	Glacier flexible retrieval 
    •	Glacier Deep Archive
    •	Glacier Instant retrieval 
  
  Storage lens 
    •	You have an organization and have s3 buckets all over the organization.
    •	S3 storage lens examines all the s3 buckets in your organization and gives you recommendations to change the storage class all over the organization.
  
  S3 lifecycle configuration
  
  S3 Intelligent Tiering

Q. What are the different data transfer costs?
Inbound costs are always free, but outbound costs are not free.

$$$- outbound traffic to the public internet.
$$- region-to-region
$- AZ-to-AZ in same region 
Free- instance-to-instance in the same AZ

Q. What is the better option to transfer the data?
If there is the possibility of transferring within the AWS cloud, that would be a better option than transferring among the internet traffic.

Q. What are the ways to monitor and predict cost on AWS?

  Pricing calculator 
    •	It is used to estimate the cost.
  
  AWS budgets 
    •	It allows you to customize budgets and you can receive alerts if you reach your alert.
    •	Alerts like SNS alerts
  
  Cost explorer
    •	Is it the dynamic visualization dashboard, where you can gain insights into the resources in different locations or regions.
    •	Can see what the cost would be at the end of the month.
  
  Cost and Usage Reports
    •	Gives you a super detailed report.
    •	Analyze the historical data.

Q. How do you manage your cost in multi-account management?
Consolidating billing - AWS organization feature.
Billing conductor - group account and generate billing.

Q. What is a tag?
Tag – group and filter your resources.

Q. What are the different types of accounts and aws supports? 
AWS support – raising tickets and receiving support form AWS support.

Basic -free
Developer- $29
Business - $100
Enterprise On-Ramp - $5500
Enterprise - $15000

Q. What are other support services?
  AWS IQ - it is the marketplace for independent freelancers and consultants who are all AWS certified.
  AWS Managed Services – pre-configured security and operations management.
  Helps to scale quickly on AWS.
  AWS professional services – A team of AWS experts who work for AWS,
  AWS Activate – it’s good for startups.



![image](https://github.com/Anuhyapeddi/aws-cloud-practitioner/assets/42506400/89211979-7bb3-4db4-a751-2a220617f056)
