# cell-emulation-util

A script based on Linux TC netem to emulate the latency, loss, and
bandwidth of a real-world cellular network.

## Usage

In order to emulate a cellular network, run the script on a network
element connection client and server:

```sh
$ ./cellular_emulation.sh <type_of_simulation> <condition>
```

The possible values for `<type_of_simulation>` are `loss_based` and
`experience_based`.

The possible condition values when `loss_based` are `good`, `median`,
and `poor`.

The possible condition values when `experience_based` are `noloss`,
`good`, `fair`, `passable`, `poor`, and `verypoor`.

So an example command would be:

```sh
$ ./cellular_emulation.sh loss_based good
```

## Background

This utility was created by Utkarsh Goel at Akamai during research for
a paper entitled "Making HTTP/2 Pages Load Faster in Lossy Cellular
Networks" authored by Utkarsh Goel, Moritz Steiner, Mike P. Wittie,
Martin Flack, and Stephen Ludin.
The
[manuscript is available](https://www.akamai.com/us/en/multimedia/documents/technical-publication/domain-sharding-for-faster-http2-in-lossy-cellular-networks.pdf)
and [detailed instructions to setup this testbed are
available](https://developer.akamai.com/blog/2017/11/27/replaying-cellular-network-characteristics-cloud-infrastructure/).

(c) Copyright 2016 Akamai Technologies, Inc. Released under Apache
License Version 2.0.
