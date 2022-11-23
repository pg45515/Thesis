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
The OSM Community makes avaiable a script file that install OSM automatically in a easy way. Following the commands below a standlone Kubernetes on a single host will be installed with OSM on top of it.

`wget https://osm-download.etsi.org/ftp/osm-12.0-twelve/install_osm.sh
chmod +x install_osm.sh
./install_osm.sh`




