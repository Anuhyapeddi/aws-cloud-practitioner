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
Q. What is continuous Integration (CI)?
Continuous Integration (CI) in AWS refers to the practice of automatically building and testing code changes whenever developers make updates to a shared code repository. AWS provides various services and tools that support CI practices, such as AWS CodePipeline, AWS CodeBuild, and AWS CodeCommit.

Q. What are the benefits of continuous Integration/ continuous Deployment?
•	Automation is good – fast, scalable, repeatable.
•	No manual effort – slow, error-prone, inconsistent.
•	Small changes applied frequently – catch bugs when they are small and simple to fix.

Q. What is continuous deployment (CD)?
Continuous Deployment (CD) in AWS is an extension of Continuous Integration (CI) where code changes that pass automated tests are automatically deployed to production environments. This means that whenever developers make changes to the codebase, those changes are automatically pushed to the production environment without manual intervention.

Q. aws development tools?
Codecommit
•	it’s like a private git repository in the cloud. 
•	It is the place to store source code, binary, images, and libraries. 
•	It receives updates from multiple places from multiple developers, so that it helps to manage, collaboration and track code changes.
•	Also maintains the version history.
Codebuild 
•	It is the fully managed build and test service. 
•	Runs the set of commands that you define, to compile code, run tests and produce the artifacts that are ready to deploy.
•	It can refer to the code, which is stored in the code commit repo and use the code to build the deployable artifacts.
Codedeploy 
•	It is the automated deployment service.
•	It automatically deploys the code in ec2 instance, on-premises, lambda.
•	Avoid downtime and avoid risks by manual processes.
Codepipeline 
•	Codecommit -> codebuild -> codedeploy -> ec2 instance

Q. what is cloud9?
Cloud9 is an integrated development environment (IDE) that you can use inside of your browser.
That means you can write, run, and debug the code, without need to install anything in your local machines.

Q. what is codeartifact?
•	An artifact repository makes it easy for the developers to find the right version of the code.
•	Artifact is called as documentation, complied applications, deployable packages, and library.
•	Supports third-party or in-house developed artifacts.
•	It is used for developers to find approved packages to public.

Q. Decoupling application components
Tight coupling 
•	Components are dependent on each other. 
•	If one fails another component will not work
Loose coupling
•	Components are not dependent.
•	If one fails, it will not affect the other.

Q. what are the integration services in aws?
Queues -> SQS
Notifications ->SNS
Events -> Eventbridge

Q. what is SNS?
•	Simple Notification Service
•	Type of messages -> SMS text messages and emails
•	Used Pub-sub model, publish the messages to the subscribers.

Q. what is SQS?
•	Simple Queue Service 
•	It is a temporary repository for messages that are waiting for processes.
•	Messages wait in the queue until the consumer is ready to process them.
•	It is pull-based service.

Q. what are the types of SQS?
Standard
•	It is the default queue type.
•	The messages are delivered at least once. 
•	It mostly maintains order, but sometimes the order gets change.
•	Sometimes it has duplicate.
FIFO
•	First in first out.
•	Strictly follows the order.
•	No duplicates.

Q. what is short polling and long polling in SQS?
Short polling 
•	It will respond immediately, even the queue is empty.
•	You need to still pay for empty responses.
Long polling
•	Queue is polled periodically.
•	It will respond Whenever the message appears in the queue, or long poll times out.
•	It is cost efficient way.

Q. what is SES?
•	Simple Email Service
•	It sends the rich formatted html mails. 
•	Always you to send mails in bulk. 

Q. what is the difference between SNS and SES?
SNS send SMS text messages and plain email to the consumers. Whereas SES send the rich formatted html emails to the consumers.

Q. what is EventBridge?
•	It uses the event-driven architecture.
•	It is simply a change in state.
•	Can handle scheduled events, which run on the schedule. 
•	If we schedule run once an hour, it runs once in hour.


Example:
For example, let's say you have an application that uploads files to an S3 bucket. You can configure S3 to send an event to EventBridge whenever a file is uploaded. Then, you can set up a rule in EventBridge to trigger a Lambda function whenever such an event occurs. This Lambda function can process the uploaded file, maybe by resizing images or extracting text, and then store the result in another S3 bucket or send it to another service.

In this example, EventBridge acts as the glue between the S3 bucket and the Lambda function, allowing you to easily create event-driven architectures without managing complex integrations.

Q. what is step function?
•	It is serverless. 
•	It automatically triggers and tracks each step.
•	It logs each step, so that it can keep track where the step when wrong.

Example:
seeing product -> hold product -> billing.

•	In each step it uses lambda.
•	Output of one step is the input of the next step.

Q. what is X-ray?
•	Provides the end-to-end view of the requests throughout your applications.
•	It is a tool to analyze, and debug distributed applications.
•	Troubleshoot the root cause of the performance issues and errors.
•	Allows you to visualize your applications underlying components.

Migration and Transfer Technology and Services
Q. snowball family?
Snowball family is used for data transfer solutions. From physical to aws cloud. 

Snowball 
•	Can hold 10 tb or more of data.
Snowball edge
•	Can hold 10 tb or more of data and need some computation process.
Snowmobile 
•	Shipping container full of disked towed by truck.
•	10 pb or more.
Snowcone 
•	Small and portable, can hold up to 14tb. 
•	Mostly used for military purpose.

Q. What is AWS Transfer family?
•	It is used to transfer files from third party to AWS storage.
•	Business-to-business file transfer protocol uses like SFTP, AS2, FTPS and FTP.
•	It uses SFTP put for storing files in storage.
•	It uses SFTP get for retrieving files from storage.

Partner -> SFTP put -> aws storage. (to store the info)
Partner -> SFTP get -> aws storage. (to get the info)

Q. What is DataSync?
•	It is used to transfer the large amount of data to aws storage.
•	Data is encrypted.

Examples:
Your datacenter -> encrypted -> s3
Other cloud provides -> encrypted -> EFS.
Aws storage services -> encrypted -> aws storage services.

Q. what is application discovery service?
•	Used to migrate bunch of applications or databases to aws.
•	Discovery tool gathers data about your existing setup. And data is collected and sent over the aws.
•	It is encrypted.
•	It is stored in migration hub.

Applications
/databases   -> application discovery service -> migration hub 

Q. How the data is collected in Application Discovery service?
•	By installing the application discovery service agent on your virtual machines or physical servers.
•	Agent gathers the data and sends to application discovery service.
•	We can also use agentless collector; it is only used for vm ware.
•	Agentless collector is installed in vmware appliance.
•	It’s running on separate virtual appliance instead of being an agent.


Agent 
Installed on 
Application      ----->   collected data ------> app discovery service.

Q. what is application migration service?
•	It is used to migrate applications to aws.
•	It automatically converts the source servers to run natively on aws.
•	It also performs the test before migrating to aws.

Q. How the applications are migrated to aws using application migrating service?
•	It is done by installing aws replication agent.
•	Application migration service performs the continuous replication form the source servers to the destinated servers.
•	Traffic is encrypted.
•	It is free to use up to 90 days.

Installing replication agent 
On our server -------------> continuous replication ----------> aws.

Q. What is Migration Hub?
•	It is the central location for managing the migration of applications and data into aws.
•	Enable to access, plan, track, and migrate to aws.
•	It is used to integrate other services like application discovery service, application migration service and database migration service.

Artificial Intelligence, Machine Learning, and Analytics Technology and Services
Q. what is redshift?
•	It is a data warehouse service.
•	Used to store large amount of data.
•	It stores the data in petabytes(pb)
•	Used for reporting and analyzing. Majorly used for business
intelligence.
•	Used for OLAP (online analytics processing)

Q. what is redshift serverless?
•	No infrastructure to manage.

Q. what is kinesis?
•	It is the service which collects and analyze the steaming data.
•	Allows you to build custom application.

Q. what is kinesis stream?
Stream data and videos which allows you to create custom application.
Kinesis data stream
•	process the streaming data.
•	It takes the produced data and store in shards.
•	Shards are data records with unique sequence number.
•	Kinesis stream is made up of one or more shards.
•	It stores data 24/7 and 365 retentions.
•	If want to do anything with data, we can provide them to database.
•	consumer like ec2 instance or lambda.
•	After the computation is done, they can send to databases like dynamo db, s3, emr, and redshift.

Producer -----> kinesis stream -----> consumer -----> database.

Mobile/laptop/ec2 -> shards in kinesis stream -> ec2/ lambda -> db.

Kinesis video stream – process the videos into aws for storage.

Q. What is kinesis data firehose?
•	It captures, transform, and loads data to aws storage. It is used to make analysis like BI visualization.
•	When the data is produced it run in kinesis firehose. If we want to store the data. We should database.
•	No shards and no retentions. Optionally we can perform lambda.
•	No consumers, it directly stores data into database like s3, OpenSearch.

Producer -----> kinesis firehose -----> database -----> warehouse.

Mobile/ec2/iot --> kinesis firehose opt lambda --> s3 --> redshift.



Q. what is the main difference between kinesis stream and kinesis firehose?
Kinesis firehoses transform and loads data in database. Whereas kinesis will directly provide to consumers.

Q. What is Amazon Athena?
•	Uses standard sql quires.
•	It is serverless.
•	It is used for querying log files and generating reports from s3.
•	It is an interactive query.

Q. What is Amazon Glue?
•	Discovery, categorize and transform the data. It is used to prepare your data for analytic and machine learning.
•	It cleans data, remove duplicates, and enrich the data and then transforms to database for analytic.
•	Catalogs your data, which category’s the data according to their type and keeps the metadata. So that the processed data is used for analytic and machine learning.

Database -----> glue ------> Database 
Database -----> glue ------> catalog (to the specific data)

Q. Steps performed by glue?
•	Performs ETL (extract, transform, load)
•	Extract data from source like s3, lambda, kinesis.
•	Transform data. Like clean, delete duplicates and join multiple data sets.
•	Load data into rds, redshift, s3 or athena.

Q. what is aws data exchange?
•	It is the service that allows you to securely exchange data between third party on subscription basis.
•	They provide the data in data product format.
•	The format can be anything which can be stored in s3. Like csv, parquet, or image files.

Q. What does Elastic map Reduce (EMR)?
•	It is the big data platform. It deals the large amount of data.
•	Large-scale parallel processing.
•	It deals data in petabyte.

Q. what kind of data does Elastic map Reduce (EMR) supports?
•	Structural data – financial transaction data.
•	Semi Structural data – text, documentation.
•	Unstructured data – application logs, click-stream data.

Q. what is Amazon OpenSearch?
OpenSearch is a software tool that helps you search and analyze large amounts of data quickly. It can be used to search through documents, logs, and other types of data to find specific information or patterns. It's often used in applications like search engines, log analysis, and data visualization.

Q. why OpenSearch is better than elastic search?
Deploying and administering your own elastic cluster can be a time consuming and complex process. Where OpenSearch service comes in.

Q. what is Managed streaming for Apache Kafka?
•	It is the service which collects and analyze the streaming data.
•	It same as kinesis but the main difference is it uses Apache Kafka.
•	The users who want to use Apache Kafka but don’t want to manage the server.

Producer -----> Apache Kafka -----> consumer
Stock price data ----> Apache Kafka <----- data consumer.

Q. What is Quick Sight?
•	Business analytic service which makes you to make better decisions on your data.
•	It can connect to aws and on-premises.
•	Visualize your data, like bar graph, line graph and plot graph.

Many businesses are storing large amount of data. Even more amount of data is produced. Among this large amount of data. How can you find which data is beneficial to you. So here comes quick sight which takes all your data and perform some methods and give you insights about your data. It gives you bar graph, line graph, plot graph.

Business data ----> quick sight -----> business decisions.

Q. what is amazon segamaker?
•	Fully managed machine learning service. It helps to import and prepare data.
•	Let’s you built your model.
•	Train your model by optimized infrastructure.
•	Deploy your model.

Import data --> built model --> train model --> deploy model.

Q. What is Amazon Kendra?
Intelligent search service that uses natural language processing to return specific answers to search questions from your data.

•	Kendra first indexes your documents. Indexes stores the contents of your data. 
•	After the index is created. You can question the Kendra using nlp and will provide the answers using data index.

Your data (s3, rds) -> indexes, Kendra -> answer from indexes.

Q. what is lex?
•	Conversational chatbots.
•	Uses nlp.

Q. what is Polly?
•	Converts text to speech.
•	Uses deep learning.

Q. what does amazon comprehend do?
•	It uses nlp and ml algorithms to process data.
•	It used for sentimental analysis – customer opinion.
•	Discovery the key phrase, topics, and languages.
•	Intelligent search – intent and context instead of keywords.

Q. what is textract, transcribe and translate?
All 3 uses machine learning algorithms.

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
Q. what is cloud watch?
CloudWatch is a monitoring and management service provided by Amazon Web Services (AWS). It helps you keep track of your AWS resources and applications by collecting and tracking metrics, monitoring log files, setting alarms, and automatically reacting to changes in your AWS resources. 

In simpler terms, CloudWatch acts like a set of eyes and ears for your AWS services, letting you know if something goes wrong or if there are opportunities to improve performance. For example, it can tell you if your server is running out of memory or if your website is receiving more traffic than usual.

To use this, you need to install cloud watch agent on ec2 instance. It also provides the dashboard.

Q. What is cloud trail? 
CloudTrail is another service provided by Amazon Web Services (AWS), but instead of monitoring your resources like CloudWatch, CloudTrail monitors and logs all actions taken on your AWS account. 

It's like having a recording of everything that happens in your account, such as who accessed it, what actions they performed, and when they did it. This information can be useful for security, auditing, and troubleshooting purposes. 

For example, if someone accidentally deletes an important file, you can use CloudTrail to see who did it and when, so you can restore the file and prevent it from happening again.

Monitors the api calls.
Track actions.

Q. What is tag?
•	It is used to sort and visualize cloud resources based on category you decide.
•	Grouping resources.
•	Tag is the key: value pair.

Q. Define systems manager?
•	It is used to organize your resources not only on aws cloud but also on-premises.
•	There is also a parameter store, where you can securely store your passwords, database string and license keys.

Q. Define aws Health dashboard?
•	Checks the health of the resources in all regions.
•	You can monitor by aws health dashboard on aws console and 
•	Another way to monitor your resources by aws health api, here you can customize your dashboard.

Q. Define Trusted Advisor?
•	Can advise on performance. 
•	Cost optimization.
•	Fault tolerance.
•	Service limits.
•	Security. 
•	Operational excellence.

Q. what are the free trusted advisor checks?
•	Do you have any open security groups?
•	Are you using IAM users?
•	Does your MFA is enabled in your account?
•	Are you getting close to your service limits?
•	Do you have any public rds snapshots?
•	Do you have any public ec2 volume snapshots?
•	Do your s3 buckets have open access? 

Q. what is aws config?
•	Pre-defined recommendations or you can set custom rules.
•	Detects defected resources and sends alerts administrators.

Q. what is Audit manager?
•	Centralize audit data form asw config and security services.
•	You can know the root causes of the defected resources and make reports.
•	Pre-defined frameworks like HIPPA, NIST cyber security 

Config, 
security hub -> audit manager + pre-defined frameworks -> reports.

Q. Rather than aws Config and aws audit manager. Are there any other tools that will audit?
Yes, well-architecture tool.

Q. what does amazon connect do?
•	Cloud-based contact center.
•	Allows you to create a call center in the cloud, this can be distributed call by agents, cases, managers all over the globe.
•	Then your manager and agent around the globe, can log into your amazon connect application and manage their work there.

Q. what is Amazon workspace?
•	Provision remote desktops for dispersed employees.
•	Create the directory of users and give them the access to the virtual desktops.

 Allocate users ---------------------> remote desktops.


Q. what is amazon AppStream?
•	Converts applications to SaaS (software as a service) for employees or end users.
•	Host and manage the application in the cloud, they can be accessed by the web-browser.
•	Package your application, load into appstream, connect users and your application is accessed by web browser. 
•	Here you no need of scaling of provisioning any resource. 

Package your application -> load into appstream -> connect users -> application is accessed by web browser. 

Security, Compliance, and Governance

Q. what is IAM (Identity Access Management)?
•	When you attach IAM policies to users, groups, and roles. They are known as Identity based policy. 
•	They give granular permissions.
•	If possible, use IAM roles because it automatically rotates access key. 

Q. what are the additional tools in IAM?
IAM access Analyzer
•	This identifies and alerts you, which user have external access to resources.
•	Validate IAM policies.
•	Generate IAM policy based on your usage.
IAM policy simulator
•	Test yourself before applying to user or groups.

Q. what is federated Identity?
•	You want your users to access to aws resources. You can do it creating IAM users like giving a unique username and password. Or it can use already existing authentication directory.
•	The process of using the existing authentication directory called federal identity, where your user can login and verify the identity.

Q. what is IAM Identity Center?
•	IAM Identity Center is the service for Federal Identity.
•	It is more secure way to give access to resources than creating IAM users. 
•	When you are giving access through IAM Identity Center and Identity Federal you are using IAM roles.
•	When the users sign-on using IAM roles, they temporarily access the resource.

Users -> identity center and identity federal -> access to resource.

Q. what is aws directory service?
•	IAM Identity Center cannot directly connect to Microsoft authentication center. It uses aws directory service.
•	It used to connect aws eco-system with an existing Microsoft authentication center.

Q. what is web federated Identity?
•	You want your users to access to your application. You can set your own authentication rules. Or you can use third party identifier.
•	Here aws provides you with web identity provider, it verifies the user identity.

Q. what is Amazon Cognito?
•	Amazon Cognito service for web identity provider.
•	Example login with google, amazon, apple.

Q. what is aws security token service (STS)?
•	Giving them a temporary access. Like read-only access for third party audit.

Q. what is encryption at rest?
encryption at rest – Encryption at rest means protecting your data in place.

Methods for encryption at rest:
Server-side encryption
•	s3 is the server-side encryption. 

Amazon Macie
•	It is another way to keep data safe in s3.
•	It uses the machine learning algorithms. 
•	It scans the s3 bucket and identify any sensitive data and PII (personal Identity Information) is existed.

Key management service 
•	KMS is used for encrypting the EBS volumes and RDS. 
•	You cannot encrypt the existing rds. For that you need to create the copy of rds and make kms for rds copy.

Q. what is encryption at transit?
encryption at transit - Encryption at transit means protecting your data while moving.

Methods for encryption at transit:
VPC (Virtual private cloud)
•	All traffic within the vpc is encrypted.

Certificate manager
•	Transferring data on http is not safe. Instead, you should use https.
•	Because https uses TLS (transport layer security) protocol
•	Certificate manager is the service helps you to automatically renew public or private TLS certificate.

Q. what are another kind of data should be kept secret?
Parameter store
•	Parameter store can securely store passwords, database string and other reference.
•	It gives the programmatic access.
•	Imagine, you have ec2 instance and want to access database. You can keep those database credentials on parameter store. Your ec2 instance only access it if they have necessary IAM role.

Systems manager
•	It’s same as parameter store but more advanced.
•	If you want to give access to ec2 instance but you don’t want to live your secrets for long. Systems manager is the best option.
•	Allows you to rotate your secrets.

Q. what is aws firewall manager?
AWS Firewall Manager is a security management service that allows you to centrally configure and manage firewall rules across your accounts and applications in AWS Organizations.

Q. what are the types of aws firewall manager?
AWS network firewall 
•	AWS Network Firewalls goes beyond the NACLs and security groups by allowing you to define the complex rules to inspect traffic coming into VPC.

AWS WAF (Web application Firewall)
•	It protects from sql injections.

AWS shield
•	It protects from DDoS (Distributed Denial of Service) Attack.
•	Shield advanced gives you 24/7 protection.

Q. what is Security Hub?
•	It supports the bunch of security and configuration services.

Q. What are the 4 security events?
AWS Trusted Advisor
•	Suggestions on Performance, security, fault tolerance, service limits, cost optimization, operational excellence.

Amazon GuardDuty
•	Tracks activity logs and finds the malicious behavior.
•	Using machine learning algorithms
•	It detects threats. 

Amazon Detective 
•	Investing the security events that are already happened.
•	Helps you to find the cause and the extent of the event.

Amazon Inspector
•	It continuously scans your workloads to detects the vulnerabilities and network exposure.
•	It also alerts you.

Q. What is AWS Organization?
•	It is used to organize all your aws accounts. 
•	Used of consolidated billing.
•	You can use config rules for detecting non-compliant resources across you entire aws organization.
•	We can also use service control policy to prevent certain actions across your organization.

Q. What is Artifact?
•	Where you can download and compliance.
Pricing, Billing, and Support
Q. what are the ways to optimize the cost?
Auto scaling 
Reserved Instance 
•	Standard Reserved Instance 
•	Convertible Reserved Instance 
•	Scheduled Reserved Instance 
Spot Instance 
Compute optimizer 
•	Compute optimizer is the way to get recommendation of your cost.
•	It uses CloudWatch logs to analyze and gives you recommendations. On how to right-size your instances.
•	It uses machine learning algorithms.
On demand Instances 
•	Lambda 
•	AWS fargate – it used for containerized workloads like Kubernetes and ECS.

Q. what are the different s3 storage?
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
•	S3 storage lens examine all the s3 buckets in your organization and gives you recommendations to change the storage class all over the organization.

S3 lifecycle configuration

S3 Intelligent Tiering

Q. What are the different data transfer cost?
Inbound cost is always free, but outbound cost is not free.

$$$- outbound traffic to the public internet.
$$- region-to-region
$- AZ-to-AZ in same region 
Free- instance-to-instance in same AZ

Q. what is the better option to transfer the data?
If there is the possibility of transferring within the aws cloud, that would be better option than the transferring among the internet traffic.

Q. what are the ways to monitor and predict cost on aws?

Pricing calculator 
•	It is used to estimate the cost.

AWS budgets 
•	It allows you to customize budgets and you can receive alerts if you reach your alert.
•	Alerts like SNS alerts

Cost explorer
•	Is it the dynamic visualize dashboard, where you can again insights of the resources on different location or regions.
•	Can see what cost would be at the end of the month.

Cost and Usage Reports
•	Gives you the super detailed report.
•	Analyze the historical data.

Q. How you manage your cost in multi-account management?
Consolidating billing - AWS organization feature.
Billing conductor - group account and generate billing.

Q. What is tag?
Tag – group and filter your resources.

Q. what are the different types of accounts and aws supports? 
AWS support – raising tickets and receive support form aws support.

Basic -free
Developer- $29
Business - $100
Enterprise On-Ramp - $5500
Enterprise - $15000

Q. what is other support services?
AWS IQ - it is the marketplace for independent freelancers and consultants that are all aws certified.
AWS Managed Services – pre-configured security and operations management.
Helps to scale quickly on aws.
AWS professional services – A team of AWS experts who work for aws,
AWS Activate – it’s good for startups.



![image](https://github.com/Anuhyapeddi/aws-cloud-practitioner/assets/42506400/89211979-7bb3-4db4-a751-2a220617f056)
