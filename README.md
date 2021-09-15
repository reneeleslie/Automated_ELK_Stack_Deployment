# Automated_ELK_Stack_Deployment
These files comprehensively show how a live ELK deployment was accomplished on Azure. This respository includes full description of the network topology, access policies, configuration of the ELK server and the details of the Ansible build.
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

https://github.com/reneeleslie/Automated_ELK_Stack_Deployment/blob/main/draft%20Network%20Diagram.jpg

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

https://github.com/reneeleslie/Automated_ELK_Stack_Deployment/blob/main/filebeat%20playbook
https://github.com/reneeleslie/Automated_ELK_Stack_Deployment/blob/main/metricbeat%20playbook

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly efficient, in addition to restricting access to the network.
Load balancers protect against DDos attacks by distributing incoming traffic to multiple servers. A jump box is able to streamline maintenance of a system by only having to update the jumpbox. 

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _____. 
Filebeat watches for log files to see 
- _TODO: What does Metricbeat record?_

The configuration details of each machine may be found below.

| Name                       | Function       | IP Address | Operating System |
|----------------------------|----------------|------------|------------------|
| Jump-Box-Provisioner       | Gateway        | 10.0.0.7   | Linux            |
| Web-1                      | Server         | 10.0.0.7   | Linux            |
| USEME-Web-2                | Server         | 10.0.0.9   | Linux            |
| ELK-server                 | ELK Server     | 10.1.0.4   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the _____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

https://github.com/reneeleslie/Automated_ELK_Stack_Deployment/blob/main/filebeat%20success.JPG
https://github.com/reneeleslie/Automated_ELK_Stack_Deployment/blob/main/metricbeat%20success.JPG

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
Web-1 10.0.0.7
USEME-Web-2 10.0.0.9 

We have installed the following Beats on these machines:
Web-1, USEME-Web-2, ELK Server
The Elk Stack installed are: Filebeat and Metricbeat

These Beats allow us to collect the following information from each machine:
Filebeat collects and sends log data which can provide access information. Metricbeat collects and sends metric data of what is running on a server which can provide information on memory and data usage.  

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the ansible configuration file to the ELK server.
- Update the ansible playbook file to include the specific servers.
- Run the playbook, and navigate to your ELK machine to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?
- You specify where to install the Elk server and the Filebeat in their respective yml files. 
URL to check that the ELK server is running: http://20.199.183.58:5601/app/kibana#/home/tutorial_directory/logging

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

