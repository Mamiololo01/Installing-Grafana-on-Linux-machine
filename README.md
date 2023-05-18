# Installing-Grafana-on-Linux-
Step by step guide to install Grafana on Linux

Grafana installation is simple and quick. Here are good to know things before you start installing Grafana:

Table of Contents	

Supported Operating Systems

Grafana supports the following databases:

Grafana has a web interface and below are the list of supported browsers:

Red Hat, CentOS, RHEL, and Fedora(64 Bit):

Supported Operating Systems
Debian / Ubuntu
RPM-based Linux (CentOS, Fedora, OpenSuse, RedHat)

macOS

Windows

Grafana requires a database to store its configuration data, such as users, data sources, and dashboards. The exact requirements depend on the size of the Grafana installation and features used.

Grafana supports the following databases:

SQLite

MySQL

PostgreSQL

By default, Grafana installs with and uses SQLite, which is an embedded database stored in the Grafana installation location.

Grafana has a web interface and below are the list of supported browsers:

Chrome/Chromium

Firefox

Safari

Microsoft Edge

Internet Explorer 11 is only fully supported in Grafana versions prior v6.0.

Grafana web URL runs on port 3000 by default. This is configurable and can be changed.

Below are the commands to install Grafana:

Ubuntu and Debian(64 Bit):

sudo apt-get install -y adduser libfontconfig1

wget https://dl.grafana.com/oss/release/grafana_6.7.3_amd64.deb

sudo dpkg -i grafana_6.7.3_amd64.deb


Standalone Linux Binaries(64 Bit):

wget https://dl.grafana.com/oss/release/grafana-6.7.3.linux-amd64.tar.gz

tar -zxvf grafana-6.7.3.linux-amd64.tar.gz


Red Hat, CentOS, RHEL, and Fedora(64 Bit):

wget https://dl.grafana.com/oss/release/grafana-6.7.3-1.x86_64.rpm

sudo yum install grafana-6.7.3-1.x86_64.rpm

OpenSUSE and SUSE:

wget https://dl.grafana.com/oss/release/grafana-6.7.3-1.x86_64.rpm

sudo rpm -i --nodeps grafana-6.7.3-1.x86_64.rpm

Configuration file(s) is stored /etc/grafana/grafana.ini If required, You can change the default port from 3000 to other port in this configuration file.

After a successful installation and configuration, you should be able to see grafana web url by going to below default link:
http://localhost:3000/grafana

If you’re running grafana on a different server and want to access it remote than use below link:
http://<<ip address>>:<<port>>
e.g. 
http://10.0.0.7:3000

Default Username and Password to access Grafana:
username: admin
password: admin

Managing Grafana Services:

sudo systemctl status grafana-server.service
sudo systemctl start grafana-server.service
sudo systemctl stop grafana-server.service
