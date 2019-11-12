# Docker xmrig Monero Ocean

Run MoneroOcean's custom XMRig Fork using Docker.

This image clones `https://github.com/MoneroOcean/xmrig` and builds it according to instructions.

## Usage

Append any `xmrig` params after the image name. i.e:

```shell
docker run -it --rm lchaia/xmrig-mo --url randomx-benchmark.xmrig.com:7777 --algo rx/test
```

## Docker Compose example

```yaml
version: "3"

services:
  xmrig:
    image: lchaia/xmrig-mo
    command: -c /xmrig/config.json --url gulf.moneroocean.stream:10001 --coin monero
    volumes:
      - ./xmrig-config.json:/xmrig/config.json
```

## Copyrights

Code from this repository is released under MIT license.
xmrig code is released under GPL-3

## Donations

Please consider [donating to the xmrig team](https://github.com/xmrig/xmrig#donations).
Also consider donating to MoneroOcean Pool, or mining on it (Zero fees!)

## Disclaimer

I'm not associated to MoneroOcean or XMRig in anyway.
