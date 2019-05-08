<!-- Auto generated file, DO NOT EDIT. Please refer to README.yml -->
# docker-base

---
![https://img.shields.io/docker/pulls/docker-base.svg](https://img.shields.io/docker/pulls/docker-base.svg)
![https://img.shields.io/github/languages/top/marcelocorreia/docker-base.svg](https://img.shields.io/github/languages/top/marcelocorreia/docker-base.svg)
![https://api.travis-ci.org/marcelocorreia/docker-base.svg?branch=master](https://api.travis-ci.org/marcelocorreia/docker-base.svg?branch=master)
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






---
[:hammer:**Created with a Hammer**:hammer:](https://github.com/marcelocorreia/hammer)
<!-- -->
















