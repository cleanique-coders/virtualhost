Virtualhost Manage Script
===========

Bash Script to allow create or delete apache/nginx virtual hosts on Ubuntu on a quick way.

## Installation ##

1. Download the script
2. Apply permission to execute:

        $ chmod +x /path/to/virtualhost.sh

3. Optional: if you want to use the script globally, then you need to copy the file to your /usr/local/bin directory, is better
if you copy it without the .sh extension:

        $ sudo cp /path/to/virtualhost.sh /usr/local/bin/virtualhost

### For Global Shortcut ###

        $ cd /usr/local/bin
        $ wget -O virtualhost https://raw.githubusercontent.com/RoverWire/virtualhost/master/virtualhost.sh
        $ chmod +x virtualhost
        $ wget -O virtualhost-nginx https://raw.githubusercontent.com/RoverWire/virtualhost/master/virtualhost-nginx.sh
        $ chmod +x virtualhost-nginx

## Usage ##

Basic command line syntax:

    $ sudo sh /path/to/virtualhost.sh [create | delete] [domain] [optional host_dir] [optional ip_address]

With script installed on /usr/local/bin

    $ sudo virtualhost [create | delete] [domain] [optional host_dir] [optional ip_address]


### Examples ###

to create a new virtual host:

    $ sudo virtualhost create mysite.dev

to create a new virtual host with custom directory name:

    $ sudo virtualhost create anothersite.dev my_dir

to create a new virtual host with custom directory name and IP Address:

    $ sudo virtualhost create anothersite.dev my_dir 127.0.0.2

to delete a virtual host

    $ sudo virtualhost delete mysite.dev

to delete a virtual host with custom directory name:

    $ sudo virtualhost delete anothersite.dev my_dir

### Localization

For Apache:

		$ sudo cp /path/to/locale/<language>/virtualhost.mo /usr/share/locale/<language>/LC_MESSAGES/

For NGINX:

		$ sudo cp /path/to/locale/<language>/virtualhost-nginx.mo /usr/share/locale/<language>/LC_MESSAGES/
