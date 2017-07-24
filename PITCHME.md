## Consul

By Hashicorp

---

## Why Service discovery?

- Monolith often evolves to SOA
- Painpoint - service discovery.

---

## What is Service discovery?

- Service A runs on node1
- Service B runs on node2
- Service A wants to call API of service B.
- "Discovers" service IP address.

---

## So far

- Maintain IPs of all services in a static file.
- Querying against a server with global configurations.
- Using DNS.
- Zookeeper, etcd - A distributed co-ordination system (KV store).

---

## Introducing consul

- First class service discovery
- Distributed, Scalable and Highly available by design. (Designed for large cluster of nodes)
- Datacenter aware.
- Health checking (routing traffic).
- An in-built KV store.

---

## Basic terminology 

_Pics on right, text on left_

- Service
- Node
- Consul agent (installed on all nodes)
	- Client
	- Server
- Server responsibilities
	- Takes part in leader elections.
	- Responsible for storing data (Service catalog) and replication.

---

## Some more

_Pics on right, text on left_

- Datacenter 
- Service catalog
- Gossip (Communication protocol).

---

## Gossip protocol

- A Cluster of nodes.
- Agents communicates to nearby agents.
- Server stores data so agents reroute to server.
- Eventually consistent.
- Uses serf library.

---

## Gossip

- LAN Gossip
- WAN Gossip

---

## Consensus protocol?

---

## Demo

- 2 Services
- Show an interaction

---

## Cluster setup

- 2 Nodes
- 2 Agents with 1 server
- Show cluster

---

## Registering

- Register a service using a file
- Show in UI that its registered.
- Show DNS API and HTTP API resolution for the service
- SIGHUP to update
- Health check
- Make service use DNS lookup to contact.
- If more than one service, show automatic failover
- consul-template to render props.

