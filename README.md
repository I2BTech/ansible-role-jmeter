jmeter
======

Installs and configures JMeter on Ubuntu 20.04.

Requirements
------------

- None

Role Variables
--------------

- `jmeter_compress_link`: string used to define URL of the zip file with the software
- `jmeter_compress_file`: string used to define the name of the zip file with the software, you can use a path relative or
absolute, if relative, the file need to be located in the files directory of the playbook.
- `jmeter_compress_content`: string used to define the name of directory inside the zip file, the jmeter home will be
linked to this directory using a soft link
- `jmeter_base`: string used to define where is the home of the user owner of the software
- `jmeter_home`: string used to define where will the software installed
- `jmeter_plugins`: List with plugins to install.

Dependencies
------------

- None

Example Playbook
----------------

```
- hosts: jmeter-host

  roles:

    - role: i2b.jmeter
      jmeter_compress_link: "https://downloads.apache.org/jmeter/binaries/apache-jmeter-5.4.1.zip"
      jmeter_compress_content: "apache-jmeter-5.4.1"
      jmeter_plugins:
        - jpgc-casutg
      tags: jmeter

```

License
-------

BSD

Author Information
------------------

IT <it@i2btech.com>
