# Homelab Documentation

Welcome to the microLab!

My goal is to have a homelab with critical services being highly available, important services being self-healing, and optional services mostly available, while maintaining a small footprint and low power consumption. Here's a photo of the current lab setup.

![microLab](/microLab.jpg)

This repo exists as part of the billv-ca/homelab-* series of repositories containing IaC and documentation for my homelab.

This repo contains documentation for the homelab-* series of repositories. See also:
- [homelab-atlantis-k3s-base-services](https://github.com/billv-ca/homelab-atlantis-k3s-base-services)
- [homelab-atlantis-k3s-services](https://github.com/billv-ca/homelab-atlantis-k3s-services)

## Hardware
### Network
#### ONT
- Provided by ISP
#### Switches
- [TL-SG1016PE](https://www.tp-link.com/ca/business-networking/easy-smart-switch/tl-sg1016pe/) (Facebook Marketplace $75 unopened)
- [Proxmox Cluster 2.5G](https://www.aliexpress.com/item/1005006821314123.html)
#### Access Points
- 3x [TP-Link Omada EAP-650](https://www.amazon.ca/dp/B0B12R9CYH)
#### Zigbee
- [SMLIGHT SLZB-06](https://aliexpress.com/item/1005004942648430.html)
#### Router
##### [Pfsense](https://www.pfsense.org/)
pfSense is a free and open source firewall and router that also features unified threat management, load balancing, multi WAN, and more.

- [HP Elitedesk 800 G3 Minis (35W)](https://support.hp.com/lt-en/product/details/hp-elitedesk-800-35w-g3-desktop-mini-pc/15234602) - [Microcad.ca $94](https://www.microcad.ca/collections/refurbished-desktops)
    - Intel® Core™ i5-6500T CPU @ 2.50GHz
    - 8GB DDR4
    - 512GB NVME
    - 1Gbe on board
    - [2.5Gbe m.2 NIC](https://www.aliexpress.com/item/1005007273213520.html) - [3d model to add nic](https://www.thingiverse.com/thing:6899748)

### Compute
- [HP Elitedesk 800 G4 Mini (35W)](https://support.hp.com/lt-en/product/details/hp-elitedesk-800-35w-g4-desktop-mini-pc/21353727) - [Microcad.ca $116](https://www.microcad.ca/collections/refurbished-desktops)
    - Intel® Core™ i5-8500T CPU @ 2.10GHz
    - 16GB DDR4
    - 256GB NVME
    - 1Gbe on board
    - [m.2 -> oculink adapter](https://www.amazon.ca/dp/B0DP4PL4JW)
    - [Minisforum DEG1 eGPU dock](https://www.amazon.ca/dp/B0DPGYKH7G)
    - [ASUS AMD 7800XT](https://www.canadacomputers.com/en/powered-by-amd/250620/asus-dual-radeon-rx-7800-xt-oc-edition-16gb-gddr6-dual-rx7800xt-o16g.html)
    - [FSP VITA 750W power supply](https://www.canadacomputers.com/en/power-supplies/253950/fsp-vita-750gm-80-gold-750-watt-atx-3-1-power-supply-vita-750gm.html)
    - [2.5Gbe m.2 NIC](https://www.aliexpress.com/item/1005007273213520.html) - [3d model to add nic](https://www.thingiverse.com/thing:6899748)

- 1 x [HP Elitedesk 800 G3 Mini (35W)](https://support.hp.com/lt-en/product/details/hp-elitedesk-800-35w-g3-desktop-mini-pc/15234602) - [Microcad.ca $94](https://www.microcad.ca/collections/refurbished-desktops)
    - Intel® Core™ i5-6500T CPU @ 2.50GHz
    - 16GB DDR4
    - 256GB NVME
    - [1TB SATA III SSD](https://www.amazon.ca/dp/B09WMP5B5N)
    - 1Gbe on board - Used for AMT
    - [2.5Gbe m.2 NIC](https://www.aliexpress.com/item/1005007273213520.html) - [3d model to add nic](https://www.thingiverse.com/thing:6899748)
- 1x [HP Elitedesk 800 G3 Mini (65W)](https://support.hp.com/lt-en/product/details/hp-elitedesk-800-65w-g3-desktop-mini-pc/15497277) - [Microcad.ca $94](https://www.microcad.ca/collections/refurbished-desktops)
    - Intel® Core™ i5-6500 CPU @ 3.20GHz
    - 24GB DDR4
    - 256GB NVME
    - [1TB SATA III SSD](https://www.amazon.ca/dp/B09WMP5B5N)
    - 1Gbe on board - Used for AMT
    - [2.5Gbe m.2 NIC](https://www.aliexpress.com/item/1005007273213520.html) - [3d model to add nic](https://www.thingiverse.com/thing:6899748)
### Power
- [APC Back-UPS ES 350VA](https://www.apc.com/ca/en/product/BE350G-CN/apc-backups-es-350va-120v-without-autoshutdown-software/)
## Software
### [Moode](https://github.com/moode-player/moode)
moOde provides a beautifully designed and responsive user interface, an extensive set of Audiophile-grade features, a reliable and stable OS and a friendly, active user Forum that provides expert troubleshooting and support, interesting discussion on a variety of audio topics and an International community of audio enthusiasts.

### [Proxmox](https://www.proxmox.com/en/products/proxmox-virtual-environment/overview)
Proxmox Virtual Environment is a complete, open-source server management platform for enterprise virtualization. It tightly integrates the KVM hypervisor and Linux Containers (LXC), software-defined storage and networking functionality, on a single platform. With the integrated web-based user interface you can manage VMs and containers, high availability for clusters, or the integrated disaster recovery tools with ease.

🔑 Integrated with Authentik

#### [OMV](https://www.openmediavault.org/)
openmediavault is the next generation network attached storage (NAS) solution based on Debian Linux. It contains services like SSH, (S)FTP, SMB/CIFS, RSync and many more ready to use. Thanks to the modular design of the framework it can be enhanced via plugins. openmediavault is primarily designed to be used in small offices or home offices, but is not limited to those scenarios. It is a simple and easy to use out-of-the-box solution that will allow everyone to install and administrate a Network Attached Storage without deeper knowledge.

#### [Home Assistant](https://www.home-assistant.io/)
Open source home automation that puts local control and privacy first. Powered by a worldwide community of tinkerers and DIY enthusiasts.

##### Add Ons
- [File Editor](https://github.com/home-assistant/addons/tree/master/configurator)
- [Music Assistant](https://www.music-assistant.io/)
- [Mosquitto](https://github.com/home-assistant/addons/tree/master/mosquitto)
- [Zigbee2MQTT](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/tree/master/zigbee2mqtt)
- [Piper](https://github.com/home-assistant/addons/blob/master/piper)
- [Whisper](https://github.com/home-assistant/addons/blob/master/whisper)

#### [Crafty Controller](https://craftycontrol.com/)
Crafty Controller is a cross platform minecraft server control platform that you control from your web browser.
#### [K3S](https://k3s.io/)
Lightweight Kubernetes. Easy to install, half the memory, all in a binary of less than 100 MB.
##### K3S Services
###### [Atlantis](https://runatlantis.io)
Terraform Pull Request Automation

🔑 Integrated with Authentik

###### [ROCm k8s-device-plugin](https://github.com/ROCm/k8s-device-plugin)
A Kubernetes device plugin implementation that enables the registration of AMD GPU in a container cluster for compute workload. With the appropriate hardware and this plugin deployed in your Kubernetes cluster, you will be able to run jobs that require AMD GPU.

###### [Ollama](https://ollama.com)
Get up and running with large language models.

###### [Open WebUI](https://openwebui.com/)
Open WebUI is an extensible, self-hosted AI interface that adapts to your workflow, all while operating entirely offline.

🔑 Integrated with Authentik

###### [Omada software controller](https://github.com/mbentley/docker-omada-controller)
Management interface and coordinator for Omada APs.

###### [Mealie](https://mealie.io/)
Mealie is an intuitive and easy to use recipe management app. It's designed to make your life easier by being the best recipes management experience on the web and providing you with an easy to use interface to manage your growing collection of recipes.

🔑 Integrated with Authentik

###### [Authentik](https://goauthentik.io/)
A self-hosted, open source identity provider means prioritizing security and taking control of your most sensitive data.

###### [Longhorn](https://longhorn.io/)
Longhorn delivers simplified, easy to deploy and upgrade, 100% open source, cloud-native persistent block storage without the cost overhead.

🔑 Integrated with Authentik

###### [Pi-hole](https://pi-hole.net/)
Network-wide protection. Instead of browser plugins or other software on each computer, install Pi-hole in one place and your entire network is protected.

🔑 Integrated with Authentik

###### [Metallb](https://metallb.io/)
MetalLB is a load-balancer implementation for bare metal Kubernetes clusters, using standard routing protocols.

###### [Kubernetes Dashboard](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/)
Dashboard is a web-based Kubernetes user interface. You can use Dashboard to deploy containerized applications to a Kubernetes cluster, troubleshoot your containerized application, and manage the cluster resources. You can use Dashboard to get an overview of applications running on your cluster, as well as for creating or modifying individual Kubernetes resources (such as Deployments, Jobs, DaemonSets, etc). For example, you can scale a Deployment, initiate a rolling update, restart a pod or deploy new applications using a deploy wizard.

Dashboard also provides information on the state of Kubernetes resources in your cluster and on any errors that may have occurred.

🔑 Integrated with Authentik

###### [Cert Manager](https://cert-manager.io/)
cert-manager is a powerful and extensible X.509 certificate controller for Kubernetes and OpenShift workloads. It will obtain certificates from a variety of Issuers, both popular public Issuers as well as private Issuers, and ensure the certificates are valid and up-to-date, and will attempt to renew certificates at a configured time before expiry.

###### [Meshcentral](https://meshcentral.com/)
The open source, multi-platform, self-hosted, feature packed web site for remote device management. 

###### [OCIS](https://owncloud.dev/ocis/)
Welcome to oCIS, the modern file-sync and share platform, which is based on our knowledge and experience with the PHP based ownCloud server.

🔑 Integrated with Authentik

###### [Wireguard](https://www.wireguard.com/)
WireGuard: fast, modern, secure VPN tunnel. WireGuard® is an extremely simple yet fast and modern VPN that utilizes state-of-the-art cryptography

###### [Wireguard UI](https://github.com/ngoduykhanh/wireguard-ui)
A web user interface to manage your WireGuard setup.

🔑 Integrated with Authentik

## Network Diagram
```
+--------+   +---+              
|FIBRE IN| > |ONT|       + > [vlan1 - LAN]
+--------+   +---+       |
               \/        + > [vlan2 - Main Wifi] > - - +--------------+
         +----------+    |                            |🛜 EAP-650(x3)|
         |🌐 Pfsense|    + > [vlan3 - IOT Wifi] >  - - +--------------+
         +----------+    |                    +------------------------------+
               \/        + > [vlan4 - lab] >  |📢 Proxmox Cluster 2.5G switch|
       +--------------+  |          \/        +------------------------------+
       |📢 TL-SG1016PE| >^ +------------------+       \/       \/       \/
       +--------------+    |📡 SMLIGHT SLZB-06| +---------+---------+---------+
                           +------------------+ |💻 node-0|💻 node-1|💻 node-2|
                                                +---------+---------+---------+
```
