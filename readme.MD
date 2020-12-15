# jitsi-census

An app to connect to a Jitsi Videobridge server and list statistical information using Colibri REST API

AUTHOR: Antonio Alisio de Meneses Cordeiro



# Usage

```sh
jitsi-census [-s <JITSI_IP_ADDRESS>] [-p <COLIBRI_TCP_PORT>] [-P <JITSI_PARAMETER_TO_SHOW>]
```
## Options

*  `-s, --server`      IP Address of the Jitsi Videobridge server. Default: localhost
*  `-s, --server`      IP Address of the Jitsi Videobridge server. Default: localhost
*  `-p, --port`        TCP port listening to the requests. Default: 8081
*  `-p, --port`        TCP port listening to the requests. Default: 8081
*  `-P, --parameter`   Parameter stats to show (comma separated). Default: show all available parameters

# Examples

## List all stats from localhosts

```sh
jitsi-census
```

## List all stats from server 192.168.0.10

```sh
jitsi-census -s 192.168.0.10
```

## Show number of 'conferences' on set server and port

```sh
jitsi-census -s 192.168.0.10 -p 8080 -P conferences
```

## Show stats for set parameters

Show stats for parameters: conferences and participants from the server 192.168.0.10 listening on port 3445

```sh
jitsi-census -s 192.168.0.10 -p 3445 -P conferences,participants
```

## Reference reading

* Jitsi: https://jitsi.org/
* Jitsi Videobridge config: https://github.com/jitsi/jitsi-videobridge/blob/master/doc/rest.md
* Jitsi Colibri: https://github.com/jitsi/jitsi-videobridge/blob/master/doc/rest-colibri.md
* XEP-0340: COnferences with LIghtweight BRIdging (COLIBRI): https://xmpp.org/extensions/xep-0340.html

## Limitations

Tested on Ubuntu 18.04 running Jitsi Meet 5142

## Development

Copyright 2020 Antonio Alisio de Meneses Cordeiro

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
