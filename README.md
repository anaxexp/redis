# Redis Docker Container Image

[![Build Status](https://travis-ci.org/anaxexp/redis.svg?branch=master)](https://travis-ci.org/anaxexp/redis)
[![Docker Pulls](https://img.shields.io/docker/pulls/anaxexp/redis.svg)](https://hub.docker.com/r/anaxexp/redis)
[![Docker Stars](https://img.shields.io/docker/stars/anaxexp/redis.svg)](https://hub.docker.com/r/anaxexp/redis)
[![Docker Layers](https://images.microbadger.com/badges/image/anaxexp/redis.svg)](https://microbadger.com/images/anaxexp/redis)

## Docker Images

❗For better reliability we release images with stability tags (`anaxexp/redis:4-X.X.X`) which correspond to [git tags](https://github.com/anaxexp/redis/releases). We strongly recommend using images only with stability tags. 

Overview:

* All images are based on Alpine Linux
* Base image: [_/redis](https://hub.docker.com/r/_/redis)
* [Travis CI builds](https://travis-ci.org/anaxexp/redis) 
* [Docker Hub](https://hub.docker.com/r/anaxexp/redis)

[_(Dockerfile)_]: https://github.com/anaxexp/redis/tree/master/Dockerfile

Supported tags and respective `Dockerfile` links:

* `4.0`, `4`, `latest` [_(Dockerfile)_]
* `3.2`, `3` [_(Dockerfile)_]

## Environment Variables

| Variable                          | Default Value           | Description |
| --------------------------------- | ----------------------- | ----------- |
| `REDIS_ACTIVE_REHASHING`          | `yes`                   |             |
| `REDIS_APPENDONLY`                | `no`                    |             |
| `REDIS_DATABASES`                 | `16`                    |             |
| `REDIS_DBFILENAME`                | `dump.rdb`              |             |
| `REDIS_LATENCY_MONITOR_THRESHOLD` | `0`                     |             |
| `REDIS_LIST_MAX_ZIPLIST_ENTRIES`  | `512`                   |             |
| `REDIS_LIST_MAX_ZIPLIST_VALUE`    | `64`                    |             |
| `REDIS_LOGFILE`                   |                         |             |
| `REDIS_LUA_TIME_LIMIT`            | `5000`                  |             |
| `REDIS_MAXMEMORY`                 | `128m`                  |             |
| `REDIS_MAXMEMORY_POLICY`          | `allkeys-lru`           |             |
| `REDIS_MAXMEMORY_SAMPLES`         | `3`                     |             |
| `REDIS_NOTIFY_KEYSPACE_EVENTS`    |                         |             |
| `REDIS_PASSWORD`                  |                         |             |
| `REDIS_SAVE_TO_DISK`              |                         |             |
| `REDIS_SAVES`                     | `900:1/300:10/60:10000` |             |
| `REDIS_SET_MAX_INTSET_ENTRIES`    | `512`                   |             |
| `REDIS_SLOWLOG_MAX_LEN`           | `32`                    |             |
| `REDIS_SLOWLOG_SLOWER_THAN`       | `10000`                 |             |
| `REDIS_TCP_BACKLOG`               | `511`                   |             |
| `REDIS_TCP_KEEPALIVE`             | `60`                    |             |
| `REDIS_TIMEOUT`                   | `300`                   |             |

## Orchestration Actions

Usage:
```
make COMMAND [params ...]
 
commands:
    check-ready host max_try wait_seconds delay_seconds
    flushall host
    
default params values:
    host localhost
    max_try 1
    wait_seconds 1
    delay_seconds 0
```

## Deployment

Deploy Redis to your server via [![AnaxExp](https://www.google.com/s2/favicons?domain=anaxexp.io) AnaxExp](https://cloud.anaxexp.io/stackhub/7548eb5a-c61b-4480-9f36-2501917692b3).

