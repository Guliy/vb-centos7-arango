# vb-centos7-arango
Vagrant box centos7 with preinstalled arangodb  

### Install
**First of all you need:**

**VirtualBox**  [dowload from this] **(http://www.virtualbox.org/wiki/Downloads)** and install.

**Vagrant** [dowload from this]**(http://downloads.vagrantup.com/)**  and install.

**Next step:**
Go to the directory with downloaded vagrant box and run from command line it:

Should be for forwarding a shared folder
```shell
$ mkdir src
```

**Adding and initializing box**
```shell
$ vagrant box add my-box package.box
$ vagrant init my-box
```

**Starting the virtual machine(VM)**
```shell
$ vagrant up --provider virtualbox
```

**Coonect to VM**
```shell
$ vagrant ssh
```

**Starting Arango server**
```shell
$ sudo /etc/init.d/arangodb start
```
The web interface can be accessed via the URL http://localhost:8529/ or http://10.10.33.10:8529 on host machine

**Starting Arango shell**
```shell
$ arangosh
```

**Stoping Arango server**
```shell
$ sudo /etc/init.d/arangodb stop
```

**Halt VM**
```shell
$ vagrant halt
```
