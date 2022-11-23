# About
Resource Orchestration in a MEC Infrastructure is a MSc in Engineering of Computer Networks and Telematic Services (MERSTel) Thesis developed in the University of Minho (UM).

# Configuration of the enviroment
## OSM Installation Process:
In order to install OSM, it is necessary, at least, a single server or a VM with the following requirements:
- 2 CPUs
- 6 GB RAM
- 40 GB disk
- 1 interface with internet access

In my case, due to hardware limitations of CPUs and memory RAM in my personal computer, the minimum required will be set.

### VM Creation:
The VM is created on **Oracle VirtualBox (version 7.0.2)** using the **Ubuntu 20.04.5 LTS server image**, available on: [Ubuntu Official Page](http://releases.ubuntu.com/20.04/)

### Installing OSM:
The OSM Community makes avaiable a script file that install OSM automatically in an easy way. Following the commands below a standlone Kubernetes on a single host will be installed with OSM on top of it.

```
wget https://osm-download.etsi.org/ftp/osm-12.0-twelve/install_osm.sh
chmod +x install_osm.sh
./install_osm.sh
```

#### Checking OSM installation:
To check if the installation was succeded, I can access to the UI using http://1.2.3.4, replacing 1.2.3.4 by the IP address of my host.

- **Username:** admin
- **password:** admin

![This is an image](/Images/Login_OSM.png)

![This is an image](/Images/Landingpage_OSM.png)

As in my case OSM is running as a Kubernetes service, it is possible to check all the running **pods**, **services**, **deployments**, **replicasets** and **statefulsets** with the command:

```
kubectl get all -n osm
```

Everything working as expected. The next step is configure the OpenStack to work as a **Virtual Infrastructure Manager** (VIM)

## OpenStack Installation Process:
Install OpenStack can be extremelly complex because OpenStack was designed to allow users to implement solutions that are tailored to their needs. To avoid this complexity, the OpenStack Community makes available DevStack - a series of scripts to quick deploy a complete enviroment based on the latest versions of everything from their [official git master](https://opendev.org/openstack/devstack)
- 2 CPUs
- 8 GB RAM
- 60 GB disk

Again, due to hardware limitations of CPUs and memory RAM in my personal computer, the minimum required will be set.

### VM Creation:
The VM is created on **Oracle VirtualBox (version 7.0.2)** using the **Ubuntu 20.04.5 LTS server image** - Ubuntu version recommended by DevStack Community - available on: [Ubuntu Official Page](http://releases.ubuntu.com/20.04/)

### Installing OpenStack (Through DevStack):
Simply follow the offical [tutorial](https://docs.openstack.org/devstack/latest/) of DevStack.



