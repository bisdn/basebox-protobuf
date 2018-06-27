# Protocol Buffer for basebox
This repository is a collection of protocol buffer used in [basebox](https://github.com/bisdn/basebox).
## Contents
The folder [common](common/) contains the proto files generated from the public yang model:
* The [empty.proto](common/empty.proto) defines a empty message.
* The [ietf-network.proto](common/empty.proto) is generated from the RFC 8345 and define the data model for the topology.
* The [openconfig-interfaces.proto](common/openconfig-interfaces) is generated from the openconfig-interfaces extension for the vlan and layer 3 information. This model is used for the statistics and the vlan configuration.
* The [ietf-vxlan.proto](common/ietf-vxlan.proto) is generated from the *draft-chen-nvo3-vxlan-yang-06* and it used to configure vxlan.

In the folder [api](api/) are defined the APIs for the vlan and vxlan configuration.

In the folder [statistics](statistics/) are defined the APIs for the statistics.

In the folder [topology](topology/) are defined the APIs for the topology.

## Protocol Buffer generation
To generate the proto file from the YANG data model, [goyang](https://github.com/openconfig/goyang) was used. Example:
```
goyang  --format proto  --proto_flat --proto_dir /path/to/protos/ --path /path/to/yang/dependencies model.yang
```
## License
In folder the [common](common/) each file is under the same license as the model from which it is generated.
The other files are licensed under the [Mozilla Public License Version 2.0](https://www.mozilla.org/en-US/MPL/2.0/). A local copy can be found [here](LICENSE.md).
