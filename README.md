# Libernet Bootstrap List

## Overview

This is a list of well-known Libernet nodes that are assumed to remain online in a stable way.

The nodes are organized by network, and for each node the IP address and port number are provided.

The list is published at the address
[https://bootstrap.libernet.io/nodes.json](https://bootstrap.libernet.io/nodes.json).

## JSON Format

The `nodes.json` file has the following format:

```json
{
  "network-name-1": {
    "chainId": 42,
    "nodes": [
      {
        "address": "123.456.789.10",
        "port": 50051
      },
      {
        "address": "321.654.987.42",
        "port": 50052
      }
      // ...
    ]
  },
  "network-name-2": {
    "chainId": 1337,
    "nodes": [
      // ...
    ]
  }
  // ...
}
```

The main object contains one entry for each network. The key is a network name (not used in the
Libernet protocol) and the value is a network object. The network object contains a numeric
`chainId` field (the network ID used in the protocol) and a `nodes` field with the list of known
nodes. Each node has an `address` and a `port`.
