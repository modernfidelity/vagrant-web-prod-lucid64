Vagrant Multi VM Environment (Ubuntu 10.04 LTS)
===============================================




This code provides VagrantFile + Puppet manifest scripts, which will create a standalone web prod environment, consisting of multi VMs, within your local development environment.

 - <a href="https://github.com/modernfidelity/vagrant-web-prod-precise64">Click here a complete version running Ubuntu 12.04 LTS</a>


Instructions
------------

- Make sure you have installed the Vagrant software : http://www.vagrantup.com/

 - Download links are here -> http://downloads.vagrantup.com/
 - For Windows users; at the time of writing this worked -> http://zamboni.readthedocs.org/en/latest/topics/install-zamboni/vagrant-on-windows.html

- Make sure you have installed Oracle VM VirtualBox : https://www.virtualbox.org/

- Make sure you have installed Ruby : http://rubyinstaller.org/downloads/

- Clone this repo and cd into the directory. 

- Run the following command : 


```bash
vagrant up
```

Softwares
---------

The following software versions are installed on the vms : 

 - Ubuntu 10.04 LTS
 - Apache 2.2.14
 - MySQL 5.1.67
 - PHP 5.3.2
 - Varnish 2.1
 - nginx 0.7.65
 - memcached 1.4.2


Machines
--------

This will then build the following vm boxes : 

- <strong>Load Balancer { varnish, niginx}</strong>
  - *33.33.33.30 (port forward 3030)*  
- <strong>2x Web { php, apache}</strong>
    - *33.33.33.31 (port forward 3031)*
    - *33.33.33.32 (port forward 3032)* 
- <strong>Database { MySQL }</strong>
    - *33.33.33.33 (port forward 3033)*


These VMs are based on Ubuntu Lucid 64 Bit => http://files.vagrantup.com/lucid64.box

Notes
-----
*Please note - you might get port errors if you are running other services on those ports. 

If this does occur you will need to either change your current service running on that specific port to another 
or amend the VagrantFile config file...
