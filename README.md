
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

<img width="901" alt="ELK_Diagram" src="https://user-images.githubusercontent.com/76065405/119424720-976fc680-bccb-11eb-9d83-e5830d35c9fc.png">


These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the elkplaybook.yml file may be used to install only certain pieces of it, such as Filebeat.


This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly redundant, in addition to restricting Denial of service to the network.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log files and system metrics.

The configuration details of each machine may be found below.

| Name              | Function | IP Address | Operating System |
|-------------------|----------|------------|------------------|
| KibaSuperJump Box | Gateway  | 10.0.0.4   | Linux            |
| KibaSuperWeb-1    | Gateway  | 10.0.0.5   | Linux            |
| KibaSuperWeb-2    | Gateway  | 10.0.0.6   | Linux            |
| ElkServer         | Gateway  | 10.1.0.4   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the KibaSuperJumpbox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:


Machines within the network can only be accessed by KibaSuperWeb-1 and KibaSuperWeb-2

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.5 10.0.0.6    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because automates away the drugery from daily tasks.

The playbook implements the following tasks:
- Install docker.io
- Install Python3
- Install Docker python module
- Increase more memory for modules to run
- Download and launch a docker elk container

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

https://github.com/GeorgeKiba/Elk-Stack-Project/blob/adb3edc4cd7c7cd8cb60e6dfc84524d370411cfb/Docker_PS.png

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- 10.0.0.5 and 10.0.0.6

We have installed the following Beats on these machines:
- filebeats and metricbeats

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc.
Download playbook - ansible-playbook (name of the playbook)
upadate playbook  - nano (name of the playbook)
