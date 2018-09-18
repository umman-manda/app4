# XMRig container

[![Docker Pulls](https://img.shields.io/docker/pulls/strm/xmrig.svg?style=plastic)](https://hub.docker.com/r/strm/xmrig/)

XMRig is a high performance Monero (XMR) CPU miner originally based on
cpuminer-multi with heavy optimizations/rewrites and removing a lot of legacy
code, since version 1.0.0 completely rewritten from scratch on C++.

## Usage

```
docker run --restart unless-stopped --name miner -d --read-only -m 50M -c 512 strm/xmrig \
   -a cryptonight -o stratum+tcp://pool.supportxmr.com:5555 -p x -k -t 2 \
   --donate-level=1 --cpu-priority 0 -u <Your Address>
```