Vagrant + Puppet
================

Modelling Your Production Environment Locally
---------------------------------------------

This provides VagrantFile + Puppet files to build a standalone web prod environment, consisting of multi VMs.

The environment consists of a Load Balancer, Multiple Webservers and a Database.

###Servers (boxes)


Available boxes are : 

 - Load Balancer { varnish, niginx}
 
 - Web { php, apache}

 - Database { percona (mysql variant) }

These are based on Ubuntu Lucid 32 Bit => http://files.vagrantup.com/lucid32.box

###Software Links

Puppet  => https://puppetlabs.com/
Vagrant => http://www.vagrantup.com/
