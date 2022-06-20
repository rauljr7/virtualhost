Virtualhost Manage Script
===========

Bash Script to allow create or delete apache/nginx virtual hosts on Ubuntu on a quick way.

## Installation ##

1. Download the script
2. Apply permission to execute:

```
$ chmod +x /path/to/virtualhost-do.sh
```

3. Optional: if you want to use the script globally, then you need to copy the file to your /usr/local/bin directory, is better
if you copy it without the .sh extension:

```bash
$ sudo cp /path/to/virtualhost-do.sh /usr/local/bin/virtualhost-do
```

### For Global Shortcut ###

```bash
cd /usr/local/bin
```
```bash
wget -O virtualhost-do https://raw.githubusercontent.com/rauljr7/virtualhost/master/virtualhost-do.sh
```
```bash
chmod +x virtualhost-do
```

## Usage ##

Basic command line syntax:

```bash
$ sudo sh /path/to/virtualhost-do.sh [create | delete] [domain] [optional host_dir]
```

With script installed on /usr/local/bin

```bash
$ sudo virtualhost-do [create | delete] [domain] [optional host_dir]
```

### Examples ###

to create a new virtual host:

```bash
$ sudo virtualhost create mysite.dev
```
to create a new virtual host with custom directory name in Digital Ocean:

```bash
$ sudo virtualhost-do create anothersite.dev my_dir
```
to delete a virtual host

```bash
$ sudo virtualhost-do delete mysite.dev
```

to delete a virtual host with custom directory name in Digital Ocean:

```
$ sudo virtualhost-do delete anothersite.dev my_dir
```
### Localization

For Apache:

```bash
$ sudo cp /path/to/locale/<language>/virtualhost.mo /usr/share/locale/<language>/LC_MESSAGES/
```

For NGINX:

```bash
$ sudo cp /path/to/locale/<language>/virtualhost-nginx.mo /usr/share/locale/<language>/LC_MESSAGES/
```
