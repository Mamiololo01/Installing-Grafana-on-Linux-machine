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

<img width="721" alt="Screenshot 2023-05-18 at 09 37 58" src="https://github.com/Mamiololo01/Installing-Grafana-on-Linux-/assets/67044030/67c1f482-e8af-4e60-b1c9-266ea9aba73a">

<img width="730" alt="Screenshot 2023-05-18 at 09 38 26" src="https://github.com/Mamiololo01/Installing-Grafana-on-Linux-/assets/67044030/8917b8d2-f7f8-4d80-8a6e-c337be6215de">

<img width="732" alt="Screenshot 2023-05-18 at 09 39 01" src="https://github.com/Mamiololo01/Installing-Grafana-on-Linux-/assets/67044030/5b228aa4-9cc5-43a6-9cfa-550f5491f1c6">

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

<img width="729" alt="Screenshot 2023-05-18 at 09 40 10" src="https://github.com/Mamiololo01/Installing-Grafana-on-Linux-/assets/67044030/9e812928-39c3-46cc-8e7e-c7dd93d2879f">

<img width="723" alt="Screenshot 2023-05-18 at 09 40 48" src="https://github.com/Mamiololo01/Installing-Grafana-on-Linux-/assets/67044030/c72c5627-90e7-4b9c-b17f-5f475807d87d">

After a successful installation and configuration, you should be able to see grafana web url by going to below default link:
http://localhost:3000/grafana

If you’re running grafana on a different server and want to access it remote than use below link:
http://<<ip address>>:<<port>>

e.g. http://10.0.0.7:3000
  
<img width="730" alt="Screenshot 2023-05-18 at 09 42 09" src="https://github.com/Mamiololo01/Installing-Grafana-on-Linux-/assets/67044030/0ed0d31a-dba4-4d38-bd8c-17542a708f60">


Default Username and Password to access Grafana:
username: admin
password: admin
  
<img width="708" alt="Screenshot 2023-05-18 at 09 43 04" src="https://github.com/Mamiololo01/Installing-Grafana-on-Linux-/assets/67044030/68607377-d418-4e5d-810e-df3f1400ac56">

Managing Grafana Services:

sudo systemctl status grafana-server.service

sudo systemctl start grafana-server.service

sudo systemctl stop grafana-server.service
