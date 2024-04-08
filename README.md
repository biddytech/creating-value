# creating-value
VPROFILE Project Setup [Local]
The objective of the project is to achieve VM Automation Locally, baseline for subsequent projects, real world project setup locally. 
This project involves multi-tier web application stack, setup on laptop/desktop and baseline for upcoming projects, deploy stack on AWS, refactor, containirize the application
We want to setup this stack locally using VM using RND
We want to hve local setup that is repeatable, automatex=d, code (IAAC)
Tools: Hypervisor (Oracle VM virtualbox),automation (vagrant),CLI (Git Bash),IDE (Sublime text)
Architecture of project services: NGINX,TOMCAT,RABBITMQ,MEMCACHED,MYSQL
Architecture of automation setup: VAGRANT,VM,GITBASH
Stack is a collection of services working together to create an experience such as web app or social networking app
NGINX is a web service  used to create load balancing experience by routing request from social netowrking app user to TOMCAT Server or Apache TOMCAT  service. Apache Tomcat is a Java application service.Java Application usually stays on TOMCAT SERVER and if there is need for external storage, NFS is used.
Username names and passwords are stored in MySQL server. MySQL server stores 
MemCached service are database caching service.
Automation stack uses Vagrant which communicates with VM Box then we will use bash script to create our services such as NGINX, APACHE TOMCAT
Flow of execution: setup tools mentioned in prerequisite video, clone video source code, cd into the vagrant dir, Bring up Vm's, Validate, Setup All the services:MySQL,MemCached,Rabbit MQ, Tomcat, NGINX, App Build & Deploy. Verify from browser.
Stack is a cobination of multiple services. Cluster is a group of systems running samne service such mySQL stack,Tomcat cluster etc
192.168.56.16	rmq01 , 192.168.56.11	web01 , 192.168.56.14	mc01 , 192.168.56.12	app01 , 192.168.56.15	db01   (vagrant-hostmanager-end ) exit
Stack is often started with AWS service such Database (MYSQL). Backend needs to be validated first and slowly go to the front end (rabbitMQ- queue/broker,Memcache(DB caching). Then application service (Tomcat) before finally coming to web service like NGINX
Vagrant ssh: You can connect to your virtual machine and confirm it is runnning by using an SSH connection: vagrant ssh. This opens a secure shell connection to the new virtual machine.
