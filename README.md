## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Image1](https://github.com/chill0516/Elk-Stack-Project/blob/main/Diagrams/TopoDiagram.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the **/etc/ansible/*.yml** file may be used to install only certain pieces of it, such as Filebeat.

  - _Note: Use the [Filebeat Configuration YML](https://github.com/chill0516/Elk-Stack-Project/blob/main/Ansible/filebeat-configuration.yml) to look at the Filebeat Configuration YML_.
  - _Note: Use the [Filebeat Playbook YML](https://github.com/chill0516/Elk-Stack-Project/blob/main/Ansible/filebeat-playbook.yml) to look at the Filebeat Playbook YML_.
  - _Note: Use the [Metricbeat Configuration YML](https://github.com/chill0516/Elk-Stack-Project/blob/main/Ansible/metricbeat-configuration.yml) to look at the Metricbeat Configuration YML_.  
- _Note: Use the [Metricbeat Configuration YML](https://github.com/chill0516/Elk-Stack-Project/blob/main/Ansible/metricbeat-playbook.yml) to look at the Metricbeat Playbook YML_.  


This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly efficient, in addition to restricting traffic to the network.
- _What aspect of security do load balancers protect?_ *Redundancy (Fault Tolerance)* 
- _What is the advantage of a jump box?_ *A jump box is a hardened and monitored device that controls access to other internal devices.*


Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the **filesystem** and system resource and **availability**.
- _What does Filebeat watch for?_ *Log files and filesystem changes.*
- _What does Metricbeat record?_ *System-level CPU usage, memory, file system, disk IO, and network IO statistics.*

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function  | IP Address  | Operating System |
|----------|-----------|-------------|------------------|
| Jump Box | Gateway   | 20.127.80.40| Linux            |
| Web-1    | Server    | 10.0.0.5    | Linux            |
| Web-2    | Server    | 10.0.0.6    | Linux            |
| TODO     | Monitoring| 10.2.0.4    | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the **jumpbox** machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _*My home network public IP address*_

Machines within the network can only be accessed by JumpBox.
- _Which machine did you allow to access your ELK VM? What was its IP address?_
*Jumpbox VM, 20.127.80.40*

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses     |
|----------|---------------------|--------------------------|
| Jump Box | Yes (SSH)           | SSH Home IP Addr         |
| Web-1    | Yes (HTTP)          | HTTP:all,SSH:10.0.0.5    |
| Web-2    | Yes (HTTP)          | HTTP:all,SSH:10.0.0.6    |
| Elk-VM   | Yes (HTTP, SSH)     | HTTP:all,SSH: 40.69.141.9|
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _The infrastructure as a code is easier to read and the revisions can be controlled._

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

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

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
