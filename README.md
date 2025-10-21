# Redis Test
For simplicity of troubleshooting Redis &amp; Redis Sentinel two docker compose files were created for each to run on a single node.

## Setup services
- One Redis master
- Two Redis slaves
- Three Redis sentinels

## Setup network
For simplicity an IPAM network was created with a subnet and an IP range for services with dynamic IP's

## File: docker-compose-IP-Addresses.yaml
This docker compose definition runs without any problems.

## File: docker-compose-Host-Names.yaml
This docker compose definition is supposed to resolve hostnames which it kind of does till you shut down the master or a sentinel.
It then goes into tilt mode and doesn't fail over even when tilt timeout is increased so any adjustments to the name service would be not fruitful.
