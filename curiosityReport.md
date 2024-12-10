
# AWS from 10,000 feet

---

## Intro

For a lot of the tool types we experimented with in class we were spoiled for choice, at least two major players with
smaller entities morefocused on particular use cases. However, I personally rarely feel comfortable burrowing deep into
an individual choice until I have at least looked at each of the options. With this mindset firmly entrenched I wanted 
to dive stright into the most twisted part of the DevOps knot and figure out roughly what all the services Amazon offers 
actually do, who uses them, for what scale and ther such questions. Giving myself a reality check after looking at the 
over 200 services on offer I tempered my views to look at everything in the categories we spent the most time in
  1. Compute (12)
  2. Containers (4)
  3. Storage (7)
  4. Database (11)
  5. Networking & Content Delivery (11)

45 services in all

## Compute

---

### EC2 (Elastic Computing Cloud)

Audience: General Developers

Purpose: Dynamically allocate computing power as directedd by policies

Services: Content Hosting, Load Balancing 

Interacts With: Security Groups 

Straightforward terminals available for rent in a variety of worldwide locations. The computers may not be in the 
clouds(most of the time) but they are out of your hair and often easier for users to get to than your machine

### Lightsail

Audience: General Developers (Cloud Beginner Friendly)

Purpose: set up and maintain a VPS (Virtual Private Server) with minimal fiddling with the settings

Services: Low Demand Content Hosting

Interacts With: Containers, Databases, Network Endpoints, Buckets, Domains

It appears to be a straightforward way to set up a simple server with minimal resource usage. The cynical side of me 
wonders how much more they charge these clients for reducing the number of options on screen and having a few good 
default settings

### Lambda

Audience: Small Flexible Cloud Computing 

Purpose: Run Specific small tasks on unspecified Amazon Hardware on demand 

Services: On Demand Cloud Computing

Interacts With: Unclear

A simple way to offload some small tasks to wherever Amazon has spare computing resources, but likely without the 
economies f scale needed for larger processing needs. It likely fills a niche

### Batch

Audience: Intermittent Exerienced Cloud Computing

Purpose: Define and Schedule Jobs to run on Amazon server instances 

Services: Scheduled Cloud Computing Resources

Interacts with: Faragate, EC2, EKS

If you're not intending to leave your cloud compute running at all times, this seems like the place to set it up

### Elastic Beanstalk

Audience: Low Hassle Developers

Purpose: Simple setup to deploy web services

Services: Servicec Management

Intercts With: App Runner, Amplify, Lightsail, Lambda, Fargate

Presents itself as "insert code, start service" probably does that well enough. No charge to use the manager, the 
benefit for Amazon is likely thaat it makes it easier for people to purchase their web services

### Serverless Application Repository

Audience: People manging multiple application instances without wanting dedicated servers

Purpose: Dashboard for application management

Services: ApplicationManagement

Interacts With: Unclear

I was suprised to see a tool with only two items on the sidebar, It exists beyond the simplicity of the easy to start
web services but has moved beyon the enormous hamburger menus of specialty options to the small targeted and refined 
group that needs a simple way to see how their serverless applicationas are doing

### AWS Outposts

Audience: Companies big enough to want their own servers but who don't want to develop their own software

Purpose: On site computing resources managed by Amazon's service programs

Services: Anything that runs on a server, but local!

Interacts With: Everything

The sales pitch is physical servers for your use only but overseen by AWS' already developed software, I'm sure there's 
a market somewhere

### EC2 Image Builder

Audience: Experienced Deployment Toolers

Purpose: Develop and Manage computer images to run on Amazon hardware as needed

Interacts with: EC2, Security Groups, Whatever you happen to need really

A practical tool for those who know the value of not having to carefully set the parameters on every virtual machine 
you want to run online

### AWS App Runner

Audience: Low Hassle Developers

Purpose: Simlified Deployment and Management assistance for web applications

interacts With: Whatever it needs, Databases, Servers, Security

A quick way to get a web application running

### AWS SimSpace Weaver

Audience: Researchers

Purpose: Run large system simultions

Interacts With: Unclear

With a simplified interface and emphasizing that it runs with "one click" This seems to be a tool targeting those that
want to simulate targets of study with the minimum amount of specializedd computing knowledge and get on to analyzing 
the output already

### EC2 Global View

Audience: Large acale developers with wide service areas

Purpose: Overview of where Elastic Computing resources are currently deployed

Interacts with: EC2

A dashboard for those with more than the average number of Cloud Computing needs with User counts high enough that the
term "region" becomes relevant

### Parallel Computing Service

Audience: Those with large computing tasks but no large computers

Purpose: easy deployment of computing heavy computing jobs

Interacts with: Its probably just EC2 under there

A service to make it easy for those with high computing needs to use Amazon's computers to fill them

## Containers

---

### ECS (Elastic Container Service)

Audience: Intermediate Deployment Developers

Purpose: Run Containerized Tasks 

Interacts with: ECR, ALB

If you know what a container is, this is the service where you hitch one up to Amazon's servers 

### EKS (Elastic Kubernetes Service)

Audience: Kubernetes Aligned Developers

Purpose: Kubernetes Clusters

Interacts With: ECR, ALB

Its ECS but for Kubernetes rather than Docker

### Red Hat OpenShift Service on AWS

Audience: Red Hat Algned Developers

Puropose: Red Hat Clusters

Interacts with: Unclear

The same as the previous two but Red Hat flavored

### ECR (Elastic Container Registry)

Audience: General Experienced Deployment Developers

Purpose: Store and Track Containerized tasks to run

Interacs with: ECS, Kubernetes, Red Hat?

If you're using containers, park them here until it's time to deploy them

## Storage

---

### S3

Audience: General Developers

Purpose: Store Data, Any kind of Data

Interacts With: *

The basic storage unit for AWS, cmes in buckets, be careful configuring security, especially with customer data

### EFS (Elastic File System)

Audience: Low Hassle Developers

Purpose: Managed Cloud File System

Services: Backup, DataSync, Data Transfer

Interacts With: *?

For those who want to store data on Amazon resources, but don't want the unusual layout of a bucket this is managed 
and likely looks just like the storage system on any standard personal computer with resources to help move data
around with less difficulty

### FSx

Audience: Low Hassle Developers and Managers in Windows Environments

Purpose: File Storage

Services: Caches, Backups

Interacts With: *?

For those wanting to save data on Amazon's cloud without the trouble of a Bucket or of using Linux

### S3 Glacier

Audience: General Developers

Purpose: Data Archive

Interacts With: * (after being unarchived S3 otherwise)

When you don't expect to need your data anytime soon, but probably shouldn't delete it

### Storage Gateway

Audience: Legacy Users of Amazon's old clouod storage portal

Purpose: Cloud Storage

Interacts With: Unclear

For those that have saved data on Amazon for years and aren't ready to deal with massive changes in accessing their
data

### AWS Backup

Audience: General Developers

Purpose: Estblish Storage Backup Policies

Services: Vaults, Jobs, Restoration, Legal Holds

Interacts With: All Other Storage Services

A single dashboard to define how your data willl respond to all of the things that can happen to data

### AWS Elastic Disaster Recovery

Audience: Developers Looking For Backup with their Backups

Purpose: Managed Data Backup Policies

Interacts With: All Other Strage Services

For those looking for some consulting and second opinions on dealing with data loss

## Database

---

### RDS (Relational Database Service)

Audience: General Developers

Purpose: Queryable Data Saved in the Cloud

Interacts With: *

A Cloud Database, pure and simple

### ElastiCache

Audience: Developers with Fast Scaling Needs

Purpose: Speed up requests of many kinds with caching policies

Interacts With: *

When Standard servers don't have enough oomph to achieve desired performance, caching can grease the wheels by moving
in-demand data closer to where its requested.

### Neptune

Audience: Heavily Query and Data-Based Applications

Purpose: Store and Manage Graphs and Other Data About Data

Interacts With: Unclear

When the queries become an unmanagable mess, this tool is there to track and save data about data about data to 
simplify analytics and analysis

### Amazon QLDB

Audience: Legcy Users

Purpose: Secure Ledgers

Interacts With: Unclear

Used until July 2025 to track transactions dealing with all of the pitfalls that includes

### Amazon DocumentDB

Audience: MongoDB Aligned Developers

Purpose: Deploy MongoDB Information and Jobs on cloud infrastructure

Interacts with: *

It's MongoDB on the cloud, it also supports elastic resizing

### Amazon Keyspaces

Audience: Apache Aligned Developers

Purpose: Cloud Apache

Interacts With: *

Do you want your Apache setup on the cloud, here is a place it could go

### Amazon Timestream

Audience: Developers with time-series data

Purpose: store and analyze time-series data

Interacts With: *

I realy don't know what else to say about this service

### DynamoDB

Audience: DynamoDB Devs

Purpose: Cloud Dynamo DB

Interacts With: *

It is at this point that I considered building a workflow to write entries about database types customly supported by
AWS, or try to write my own Database scheme and see if suddenly support would appear on AWS. All that aside, AWS 
supports DynamoDB instances

### Amazon MemoryDB

same as the first, but MemoryDB flavored

### Amazon Aurora DSQL

Wait, this ones Distributed perhas at some future I will understand the amazing feat that truly is

### Oracle Database@AWS

Huh, I guess Oracle wrote their own databse software

## Networking & Content Delivery

---

### VPC (Virtual Private Cloud)

Audience: Intermediate Developers

Purpose: Make AWS resources available only to services that use them

To connect AWS resources to user facing services with the minimum available surface, VPC is the way to go

### CloudFront

Audience: General Developers

Purpose: CDN (Cloud Delivery Network)

Useful for getting webpages where they need to go pretty efficiently

### API Gateway

Audience: General Developers

Purpose: track API endpoints adn generate SDK's

With all the services running here, we definitely need some API's, Is this the bset tool for that job, I know that I 
don't know right now

### Direct Connect

Audience: Efficiency and Security Conscious big AWS users

Purpose: set up direct connections with AWS internal network

If that's where all your stuff is and you need it fast and don't want your ISP seeign everything here's where you ask 
for that

### AWS App Mesh

Audience: Microservice Affictionadoes

Purpose: tracking microservice status

I tend to prefer the monolith model, but for those looking for a lot of simle processes, care and feeding of them can 
go on here

### Global Accelerator

Audience: Multi Region Applictions

Purpose: manage I addresses and routing to improve application response time

I was suprised that this wasn't just a subMenu on a job somewhere, maybe it usedd to be, but now its it's own tool

### AWS Cloud Map

Audience: General Developers

Purpose: Dashboard for cloud resources

A refreshingly simple layout showing what things are currently running and available in your AWS managed space 

### Amazon Application Recovery Controller

Audience: Absolute Minimum Downtime Project Developers

Purpose: direct resources to handle recovery appropriately

It is a seemingly simple thing keeping a service running, until it is crippledd and everything is fallign over, here's
where you plan your emergency crutches

### AWS Private 5G

Do You want 5G hardware, we have it

### Route 53

Audience: General Developer

Purpose: Handle DNS records for AWS services

Interacts With: Everything

As these are Web services, making sure they exist at the appropriate web locations is pretty important though it 
sounds like an old diner, Route 53 is where ll those records and domains are handled

### AWS Data Transfer Terminal

I Don't know what this does, but it only works in Oregon
