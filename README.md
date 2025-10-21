# Redis Test
For simplicity of troubleshooting Redis &amp; Redis Sentinel two docker compose files were created for each to run on a single node.

## Setup
One Redis master and two Redis slaves
Three Redis sentinels

## docker-compose-IP-Addresses.yaml
This file runs without any problems.

## docker-compose-Host-Names.yaml
This file is supposed to resolve hostnames which it kind of does till you shut down the master or a sentinel.
It then goes into tilt mode and doesn't f fail over even when tilt timeout is increased so any adjustments to the name service would be not fruitful.
