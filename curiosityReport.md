
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

An awkward unplanned 69 services in all

## Compute

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
