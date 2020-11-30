# RedisJSON port for Windows

This is a Windows port of RedisJSON (former ReJSON) module for [Redis for Windows](https://github.com/tporadowski/redis), now at version 1.0.6.
It seems to be working with both [4.0.14.2](https://github.com/tporadowski/redis/releases/tag/v4.0.14.2)
and [5.0.10](https://github.com/tporadowski/redis/releases/tag/v5.0.10), but since it was mostly ported for testing the module support in Redis for Windows - it
needs to be thoroughly tested before being used in production.

**NOTE**: below is the original Readme of [RedisJSON v1.0.6](https://github.com/RedisJSON/RedisJSON/tree/v1.0.6)


# RedisJSON - a JSON data type for Redis

RedisJSON is a [Redis](http://redis.io/) module that implements [ECMA-404 The JSON Data Interchange Standard](http://json.org/) as a native data type. It allows storing, updating and fetching JSON values from Redis keys (documents).

Primary features:

* Full support of the JSON standard
* [JSONPath](http://goessner.net/articles/JsonPath/)-like syntax for selecting element inside documents
* Documents are stored as binary data in a tree structure, allowing fast access to sub-elements
* Typed atomic operations for all JSON values types

## Quickstart

1.  [Launch RedisJSON with Docker](http://redisjson.io#launch-redisjson-with-docker)
1.  [Use RedisJSON from **any** Redis client](http://redisjson.io#using-redisjson), e.g.:

![RedisJSON with `redis-cli`](docs/images/demo.gif)

## Documentation

Read the docs at http://redisjson.io

## Current limitations and known issues

* Searching for object keys is O(N)
* Containers are not scaled down after deleting items (i.e. free memory isn't reclaimed)
* Numbers are stored using 64-bit integers or doubles, and out of range values are not accepted

## Acknowledgements

RedisJSON is developed with <3 at [Redis Labs](https://redislabs.com).

RedisJSON is made possible only because of the existance of these amazing open source projects:

* [jsonsl](https://github.com/mnunberg/jsonsl)
* [redis](https://github.com/antirez/redis)

## License

Redis Source Available License Agreement - see [LICENSE](LICENSE)

