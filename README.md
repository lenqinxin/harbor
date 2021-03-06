# Harbor

[![Build Status](https://travis-ci.org/goharbor/harbor.svg?branch=master)](https://travis-ci.org/goharbor/harbor)
[![Coverage Status](https://coveralls.io/repos/github/goharbor/harbor/badge.svg?branch=master)](https://coveralls.io/github/goharbor/harbor?branch=master)
[![Go Report Card](https://goreportcard.com/badge/github.com/goharbor/harbor)](https://goreportcard.com/report/github.com/goharbor/harbor)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/2095/badge)](https://bestpractices.coreinfrastructure.org/projects/2095)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/c8d726c9cfd047ffaf681449d673f246)](https://www.codacy.com/app/goharbor/harbor?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=goharbor/harbor&amp;utm_campaign=Badge_Grade)

**Note**: The `master` branch may be in an *unstable or even broken state* during development.
Please use [releases](https://github.com/vmware/harbor/releases) instead of the `master` branch in order to get stable binaries.

<img alt="Harbor" src="docs/img/harbor_logo.png">

Project Harbor is an an open source trusted cloud native registry project that stores, signs, and scans content. Harbor extends the open source Docker Distribution by adding the functionalities usually required by users such as security, identity and management. Having a registry closer to the build and run environment can improve the image transfer efficiency. Harbor supports replication of images between registries, and also offers advanced security features such as user management, access control and activity auditing.

Harbor is hosted by the [Cloud Native Computing Foundation](https://cncf.io) (CNCF). If you are an organization that wants to help shape the evolution of cloud native technologies, consider joining the CNCF. For details about who's involved and how Harbor plays a role, read the CNCF
[announcement](https://www.cncf.io/blog/2018/07/31/cncf-to-host-harbor-in-the-sandbox/).

### Features

* **Role based access control**: Users and repositories are organized via 'projects' and a user can have different permission for images under a project.
* **Policy based image replication**: Images can be replicated (synchronized) between multiple registry instances, with auto-retry on errors. Great for load balancing, high availability, multi-datacenter, hybrid and multi-cloud scenarios.
* **Vulnerability Scanning**: Harbor scans images regularly and warns users of vulnerabilities.
* **LDAP/AD support**: Harbor integrates with existing enterprise LDAP/AD for user authentication and management.
* **Image deletion & garbage collection**: Images can be deleted and their space can be recycled.
* **Notary**: Image authenticity can be ensured.
* **Graphical user portal**: User can easily browse, search repositories and manage projects.
* **Auditing**: All the operations to the repositories are tracked.
* **RESTful API**: RESTful APIs for most administrative operations, easy to integrate with external systems.
* **Easy deployment**: Provide both an online and offline installer.

### Install & Run

**System requirements:**

**On a Linux host:** docker 17.03.0-ce+ and docker-compose 1.10.0+ .

Download binaries of **[Harbor release ](https://github.com/vmware/harbor/releases)** and follow **[Installation & Configuration Guide](docs/installation_guide.md)** to install Harbor.

If you want to deploy Harbor on Kubernetes, please use the **[Harbor chart](https://github.com/goharbor/harbor-helm)**.

Refer to **[User Guide](docs/user_guide.md)** for more details on how to use Harbor.

### Community

**Twitter:** [@project_harbor](https://twitter.com/project_harbor)  
**User Group:** Join Harbor user email group: [harbor-users@googlegroups.com](https://groups.google.com/forum/#!forum/harbor-users) to get update of Harbor's news, features, releases, or to provide suggestion and feedback. To subscribe, send an email to [harbor-users+subscribe@googlegroups.com](mailto:harbor-users+subscribe@googlegroups.com) .  
**Developer Group:** Join Harbor developer group: [harbor-dev@googlegroups.com](https://groups.google.com/forum/#!forum/harbor-dev) for discussion on Harbor development and contribution. To subscribe, send an email to [harbor-dev+subscribe@googlegroups.com](mailto:harbor-dev+subscribe@googlegroups.com).  
**Slack:** Join Harbor's community for discussion and ask questions: [Cloud Native Computing Foundation](https://slack.cncf.io/), channel: #harbor and #harbor-dev

### Additional Tools

Tools layered on top of Harbor and contributed by community.

* **[Harbor.Tagd](https://github.com/HylandSoftware/Harbor.Tagd)**
  - Automates the process of cleaning up old tags from your Harbor container registries.
  - Lead by [@nlowe](https://github.com/nlowe) from HylandSoftware.

### Demos

* **[Live Demo](https://demo.goharbor.io)** - A demo environment with the latest Harbor stable build installed. If you want to deeply dive, please refer to **[Demo Server](docs/demo_server.md)** for more details.
* **[Video Demos](https://github.com/goharbor/harbor/wiki/Video-demos-for-Harbor)** - Demos for Harbor features and continuously updated.

### Partners and Users

If you want to learn Harbor partners and users, please refer to [list of Harbor partners and users](partners.md).

### License

Harbor is available under the [Apache 2 license](LICENSE).

This project uses open source components which have additional licensing terms.  The official docker images and licensing terms for these open source components can be found at the following locations:

* Photon OS 1.0: [docker image](https://hub.docker.com/_/photon/), [license](https://github.com/vmware/photon/blob/master/COPYING)
