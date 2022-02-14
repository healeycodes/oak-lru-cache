# oak-lru-cache

[![CI](https://github.com/healeycodes/oak-lru-cache/actions/workflows/test.yml/badge.svg)](https://github.com/healeycodes/oak-lru-cache/actions/workflows/test.yml)

A least recently used (LRU) cache written in [Oak](https://oaklang.org/).

Usage:

```
{
	lru: lru
} := import('lru')

cache := lru(5) // Max keys
cache.set('foo', 'bar')
cache.get('foo')
```

Benchmarks (run in CI):

```text
Inserted 1 key in:  0.018358230590820312 ms
Inserted 100 keys in:  1.4066696166992188 ms
Inserted 10000 keys in:  119.19784545898438 ms
Each lru.set() call took 0.013117778301239013 ms (avg) over 100000 entries
```

## Tests

```bash
vendor/oak-linux-v0.1 lru.test.oak
```

## Benchmarks

```bash
vendor/oak-linux-v0.1 lru.bench.oak
```
