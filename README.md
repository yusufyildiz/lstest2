[![Open Source](https://github.com/yusufyildiz/lstest2/blob/master/img/Linstor-Logo-Colour.png?raw=true)](https://opensource.org/)

[![LINSTOR Powered by LINBIT](https://github.com/yusufyildiz/lstest2/blob/master/img/poweredby_linbit_small.png?raw=true)](https://www.linbit.com/linstor/)   [![GitHub stars](https://img.shields.io/github/stars/linbit/linstor-server?style=social)](https://github.com/LINBIT/linstor-server/) [![Twitter](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Ftwitter.com%2Flinbit)]()  

[![Open Source](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://opensource.org/) [![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-brightgreen.svg)](https://opensource.org/licenses/) [![Slack Channel](https://img.shields.io/badge/Slack-Channel-brightgreen)](https://join.slack.com/t/linbit-community/shared_invite/enQtOTg0MTEzOTA4ODY0LTFkZGY3ZjgzYjEzZmM2OGVmODJlMWI2MjlhMTg3M2UyOGFiOWMxMmI1MWM4Yjc0YzQzYWU0MjAzNGRmM2M5Y2Q) [![Support](https://img.shields.io/badge/$-support-12a0df.svg?style=flat)](https://www.linbit.com/contact-us/) [![Active](http://img.shields.io/badge/Status-Active-green.svg)](https://linbit.com/linstor) [![GitHub Release](https://img.shields.io/github/release/linbit/linstor-server.svg?style=flat)]() [![GitHub Commit](https://img.shields.io/github/commit-activity/y/linbit/linstor-server)]() 

 
 
# What is LINSTOR;

LINSTOR developed by LINBIT, is a software that manages DRBD replicated LVM/ZFS volumes across a group of machines. It maintains DRBD configuration on the participating machines. It creates/deletes the backing LVM/ZFS volumes. It automatically places the backing LVM/ZFS volumes among the participating machines. 
LINSTOR supports [Kubernetes](https://www.linbit.com/kubernetes/), [Openstack](https://www.linbit.com/openstack/), [Open Nebula](https://www.linbit.com/opennebula/), [Openshift](https://www.linbit.com/openshift-persistent-container-storage-support/), [VMware](https://www.linbit.com/linstor-vsan-software-defined-storage-for-vmware%e2%80%8b/). 

# How it works;

LINSTOR system consists of multiple server and client components.
A LINSTOR controller manages the configuration of the LINSTOR cluster and all of its managed storage resources.
The LINSTOR satellite component manages creation, modification and deletion of storage resources on each node that provides or uses storage resources managed by LINSTOR.
The storage system can be managed by directly using a command line utility to interact with the active LINSTOR controller. Alternatively, users may integrate the LINSTOR system into the storage architecture of other software systems, such as Kubernetes.
All communication between LINSTOR components uses LINSTOR’s own network protocol, based on TCP/IP network connections.

 [![](https://github.com/yusufyildiz/lstest2/blob/master/How-It-Works2.png?raw=true)]()  [![](https://mldatnmifxoe.i.optimole.com/Q4Tiw9A-22SC98Y2/w:450/h:402/q:auto/https://www.linbit.com/wp-content/uploads/2020/03/unnamed.png)]()

# Benefits;
  - Manage Storage Volumes With Ease
  - Save Engineering Time 
  - Save Engineering Headaches 
  - Save Your Business Data 
  - Protect Your Investments 


# Features;
  - Provides replicated block storage and persistent container storage
  - Open Source
  - Integration to Kubernetes through the CSI driver., External Provisioner, Docker and Proxmox VE
  - Compatible with high I/O workloads like databases
  - Network replication through DRBD integration
  - LVM Snapshot Support
  - LVM Thin Provisioning Support
  - Online live migration of backend storage
  - RDMA
  - Management of persistent Memory (PMEM)
  - Scale-up and scale-out
  - Storage tiering (multiple storage pools)
  - Replicate via multiple network cards
  - Automatic management of TCP/IP port range, minor number range etc. provides consistent data
  - Choose your own Linux filesystem
  - Separation of Data & Control plane
  - ZFS support
  - NVME over Fabrics
  - Rest API
  - LDAP Authentification


### User Guide
You need at least 3 nodes to use LINSTOR. Linstor-controller role must be installed on one node and all nodes must be installed with linstor-satellite, and linstor-client.

LINSTOR can also perform disk operations without using DRBD. However, if replication with DRBD is desired, DRBD 9 must be installed on all servers. For DRBD installation, please follow [this link](https://www.linbit.com/drbd-user-guide/drbd-guide-9_0-en/).

For a more detailed installation guide, please follow the link below.

[![LINSTOR GUIDE](https://img.shields.io/badge/LINSTOR-GUIDE-orange)](https://www.linbit.com/user-guides/) 


### Plugins

LINSTOR is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| linstor-iscsi | [https://github.com/LINBIT/linstor-iscsi][PlDb] |


### Support

LINSTOR is an open source software. You can use our slack channel above link to get support for individual use and development use.
If you are going to use it in enterprise and mission critical environments, please contact us via the link below for professional support.

[![LINSTOR Support](https://img.shields.io/badge/LINSTOR-SUPPORT-brightgreen)](https://www.linbit.com/support/) 


### Releases
Releases generated by git tags on github are snapshots of the git repository at the given time. You most likely do not want to use these. They might lack things such as generated man pages, the configure script, and other generated files. If you want to build from a tarball, use the ones [provided by us](https://www.linbit.com/en/drbd-community/drbd-download/) .



### Building
Gradle is used for building linstor. On a fresh git clone some protobuf java files need to be generated and for that a fitting proto compiler is needed. So before building you need to run:
```sh
$ gradle getProtoc
```
After the correct proto compiler is installed in the ./tools directory you can build with:
```sh
$ gradle assemble
```
### Development
Please check the development documentation for details.  

[![LINSTOR Development](https://img.shields.io/badge/LINSTOR-DEVELOPMENT-brightgreen)](https://github.com/LINBIT/linstor-server/blob/master/docs/development.md
) 

**Free Software, Hell Yeah!**
