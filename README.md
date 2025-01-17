# Installing Grafana on a Linux Machine

This guide provides step-by-step instructions to install Grafana on a Linux machine. Grafana is an open-source platform for monitoring and observability. 

## Table of Contents
- [Introduction](#introduction)
- [Supported Operating Systems](#supported-operating-systems)
- [Supported Databases](#supported-databases)
- [Supported Browsers](#supported-browsers)
- [Installation](#installation)
  - [Ubuntu and Debian](#ubuntu-and-debian-64-bit)
  - [Standalone Linux Binaries](#standalone-linux-binaries-64-bit)
  - [Red Hat, CentOS, RHEL, and Fedora](#red-hat-centos-rhel-and-fedora-64-bit)
  - [OpenSUSE and SUSE](#opensuse-and-suse)
- [Configuration](#configuration)
- [Accessing Grafana](#accessing-grafana)
- [Managing Grafana Services](#managing-grafana-services)
- [Default Credentials](#default-credentials)
- [Resources](#resources)

## Introduction
Grafana installation is simple and quick. Before you start installing Grafana, it's good to know the supported operating systems, databases, and browsers.

## Supported Operating Systems
Grafana supports the following operating systems:
- Debian / Ubuntu
- RPM-based Linux (CentOS, Fedora, OpenSuse, RedHat)
- macOS
- Windows

## Supported Databases
Grafana requires a database to store its configuration data, such as users, data sources, and dashboards. The exact requirements depend on the size of the Grafana installation and features used. Grafana supports the following databases:
- SQLite (default)
- MySQL
- PostgreSQL

By default, Grafana installs with and uses SQLite, an embedded database stored in the Grafana installation location.

## Supported Browsers
Grafana has a web interface and supports the following browsers:
- Chrome/Chromium
- Firefox
- Safari
- Microsoft Edge
- Internet Explorer 11 (only fully supported in versions prior to v6.0)

## Installation

### Ubuntu and Debian (64 Bit)
1. Install dependencies:
   ```sh
   sudo apt-get install -y adduser libfontconfig1

## Download and install Grafana:

wget https://dl.grafana.com/oss/release/grafana_6.7.3_amd64.deb

sudo dpkg -i grafana_6.7.3_amd64.deb

Standalone Linux Binaries (64 Bit)

## Download and extract Grafana:

wget https://dl.grafana.com/oss/release/grafana-6.7.3.linux-amd64.tar.gz
tar -zxvf grafana-6.7.3.linux-amd64.tar.gz

Red Hat, CentOS, RHEL, and Fedora (64 Bit)

## Download and install Grafana:

wget https://dl.grafana.com/oss/release/grafana-6.7.3-1.x86_64.rpm
sudo yum install grafana-6.7.3-1.x86_64.rpm
OpenSUSE and SUSE

## Download and install Grafana:

wget https://dl.grafana.com/oss/release/grafana-6.7.3-1.x86_64.rpm
sudo rpm -i --nodeps grafana-6.7.3-1.x86_64.rpm

## Configuration

The configuration file is stored at /etc/grafana/grafana.ini. If required, you can change the default port from 3000 to another port in this configuration file.

## Accessing Grafana

After a successful installation and configuration, you should be able to access Grafana via the following URL:

Local access: http://localhost:3000/grafana

Remote access: http://:

## Default Credentials
The default username and password to access Grafana are:

Username: admin
Password: admin

## Managing Grafana Services

Use the following commands to manage the Grafana services:

sudo systemctl status grafana-server.service
sudo systemctl start grafana-server.service
sudo systemctl stop grafana-server.service

## Resources

Grafana Documentation

Grafana Downloads

Feel free to open an issue or contact the maintainers if you have any questions or need assistance.

