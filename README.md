# Fuel Plugin ScaleIO on Cinder for OpenStack

### Contents

- [Introduction](#Introduction)
- [Requirements](#requirements)
- [Limitations](#limitations)
- [Configuration](#configuration)
- [Contributions](#contributing-to-the-fuel-plugin-for-scaleIO)
- [License](#licensing)


## Introduction

Fuel plugin for ScaleIO for enabling OpenStack to work with an **External** ScaleIO deployment. This ScaleIO plugin for Fuel extends Mirantis OpenStack functionality by adding support for ScaleIO block storage.

ScaleIO is a software-only solution that uses existing servers' local disks and LAN to create a virtual SAN that has all the benefits of external storage—but at a fraction of cost and complexity. ScaleIO utilizes the existing local internal storage and turns it into internal shared block storage.


## Requirements

**[TODO]**


| Requirement                                              | Version/Comment |
|----------------------------------------------------------|-----------------|
| Mirantis OpenStack compatibility                         | >= 6.1          |
| Access to ScaleIO via cinder-volume node          |                 |
| Access to ScaleIO  via compute/cinder-volume nodes |                 |
| iSCSI initiator on all compute/cinder-volume nodes       |                 |


## Limitations

Currently Fuel doesn't support multi-backend storage.


## Configuration

**[TODO]**


Before starting a deployment there are some things that you should verify:

1. Your ScaleIO Cluster can route 10G Storage Network to all Compute nodes
   as well as the Cinder Control/Manager node.
2. Create an account on the ScaleIO cluster to use as the OpenStack Administrator
   account (use the login/password for this account as san_login/password settings).
3. Obtain the IP address from the ScaleIO cluster

### ScaleIO Cinder plugin installation

**[TODO]**

All of the needed code for using SclaeIO in an OpenStack deployment is
included in the upstream OpenStack distribution.  There are no additional
libraries, software packages or licenses.

### ScaleIO Cinder plugin configuration

**[TODO]**





## Contributing to the Fuel plugin for ScaleIO

The Fuel plugin for ScaleIO project has been licensed under the  [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0") License. In order to contribute to the  project you will to do two things:


1. License your contribution under the [DCO](http://elinux.org/Developer_Certificate_Of_Origin "Developer Certificate of Origin") + [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0")
2. Identify the type of contribution in the commit message


### 1. Licensing your Contribution:

As part of the contribution, in the code comments (or license file) associated with the contribution must include the following:

Copyright [yyyy] [name of copyright owner]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

This code is provided under the Developer Certificate of Origin- [Insert Name], [Date (e.g., 1/1/15]”


**For example:**

A contribution from **Joe Developer**, an **independent developer**, submitted in **May 15th of 2015** should have an associated license (as file or/and code comments) like this:

Copyright (c) 2015, Joe Developer

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

This code is provided under the Developer Certificate of Origin- Joe Developer, May 15th 2015”

### 2. Identifying the Type of Contribution

In addition to identifying an open source license in the documentation, **all Git Commit messages** associated with a contribution must identify the type of contribution (i.e., Bug Fix, Patch, Script, Enhancement, Tool Creation, or Other).


## Licensing

The fuel plugin for ScaleIO is licensed under the  [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0") license

Copyright (c) 2015, EMC Corporation

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


## Support

Please file bugs and issues at the Github issues page. For more general discussions you can contact the EMC Code team at <a href="https://groups.google.com/forum/#!forum/emccode-users">Google Groups</a> or tagged with **EMC** on <a href="https://stackoverflow.com">Stackoverflow.com</a>. The code and documentation are released with no warranties or SLAs and are intended to be supported through a community driven process.