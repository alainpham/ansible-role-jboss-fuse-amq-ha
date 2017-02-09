Ansible role for JBoss Fuse/A-MQ with minimal high availability install and configuration
=========

What this ansible role does
------------
This ansible role allows to quickly install, configure and start a small Integration Platform with JBoss Fuse and Active-MQ.
This architecture is suitable to mosts uses cases out there who want to start building an Integration Platform.
It allows to
 - ensure high availability with quick a quick fail-over mechanism
 - load balancing among active nodes
 - start small with the possibility to scale up indefinitely when needed

![overview](https://raw.githubusercontent.com/alainpham/ansible-role-jboss-fuse-amq-ha/master/meta/minimal-fuse-amq-ha.png)

The example playbook in the test folder shows how to use this role to setup the following minimal Highly Available Fuse/AMQ cluster:
- 2 machines with Active JBoss Fuse installed 
- 2 machines with A-MQ installed:
    - 2 networked master/slave couples
	- the masters share their storage with their slave instances

	

How to use it
------------
A complete playbook example can be found in the test folder.

- Download JBoss Fuse and/or AMQ packages and place them into the folder "distrib"
- Change inventory,group_vars and host_vars to your environment
- Run your ansible playbook

