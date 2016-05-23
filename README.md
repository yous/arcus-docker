# Arcus Docker

Docker for [Arcus Cache Cloud](https://github.com/naver/arcus). You can see the
repository on [yous/arcus](https://hub.docker.com/r/yous/arcus/).

## About

- CentOS 6
- OpenJDK 1.7.0
- `git`, `svn`, `wget`, `curl`, `ps`

## Installation

``` sh
docker pull yous/arcus
```

## Usage

``` sh
docker run -i -t yous/arcus:latest
```

## Quick Start

``` sh
docker run -i -t yous/arcus:latest
```

Then set up with `arcus.sh`:

``` sh
cd scripts
# Setup a local cache cloud with conf file
./arcus.sh quicksetup conf/local.sample.json

# Test
echo "stats" | nc localhost 11211 | grep version
STAT version 1.9.5
echo "stats" | nc localhost 11212 | grep version
STAT version 1.9.5
```

## License

Copyright © Chayoung You. See [LICENSE.txt](LICENSE.txt) for details.
