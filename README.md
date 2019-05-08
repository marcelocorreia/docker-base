<!-- Auto generated file, DO NOT EDIT. Please refer to README.yml -->
# docker-base

---
![https://img.shields.io/docker/pulls/marcelocorreia/docker-base.svg](https://img.shields.io/docker/pulls/marcelocorreia/docker-base.svg)
![https://img.shields.io/github/languages/top/marcelocorreia/docker-base.svg](https://img.shields.io/github/languages/top/marcelocorreia/docker-base.svg)
![https://api.travis-ci.org/marcelocorreia/docker-base.svg?branch=master](https://api.travis-ci.org/marcelocorreia/docker-base.svg?branch=master)
![https://img.shields.io/github/release/marcelocorreia/docker-base.svg?flat-square](https://img.shields.io/github/release/marcelocorreia/docker-base.svg?flat-square)
---
### TLDR;
- [Overview](#overview)
- [Description](#description)
- [Dockerfile](#dockerfile)
- [Usage](#usage)
- [License](#license)
### Overview
### Docker Base images:
- alpine
- jessie-slim
- buster-slim





### Usage
```bash
$ docker run --rm marcelocorreia/base:alpine bash
$ docker run --rm marcelocorreia/base:jessie-slim bash
$ docker run --rm marcelocorreia/base:buster-slim bash
```
## Setting timezone
```bash
$ docker run --rm -e TZ=Australia/Sydney marcelocorreia/base bash
```
### Extending
```Dockerfile
FROM marcelocorreia/base:alpine
...
```
```Dockerfile
FROM marcelocorreia/base:jessie-slim
...
```
```Dockerfile
FROM marcelocorreia/base:buster-slim
...
```
**Targets**
```bash
$ make release
$ make build
$ make push
$ make all-versions
$ make current-version
$ make next-version
```




## Dockerfile.alpine 
```Dockerfile
FROM alpine:3.9

MAINTAINER marcelo correia <marcelo@correia.io>

RUN apk update
RUN set -ex && \
    apk add --no-cache --update \
        bash \
        tzdata \
        git

CMD ["uname","-a"]
```
## Dockerfile.jessie-slim 
```Dockerfile
FROM debian:jessie-slim

MAINTAINER marcelo correia <marcelo@correia.io>

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install curl git tzdata -y

```
## Dockerfile.buster-slim 
```Dockerfile
FROM debian:buster-slim

MAINTAINER marcelo correia <marcelo@correia.io>

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install curl git tzdata -y

```



---
[:hammer:**Created with a Hammer**:hammer:](https://github.com/marcelocorreia/hammer)
<!-- -->
















