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
Inserted 1 key in:  0.02002716064453125 ms
Inserted 100 keys in:  2.0613670349121094 ms
Inserted 10000 keys in:  147.57990837097168 ms
Each lru.set() call took 0.013721413612365722 ms (avg) over 100000 entries
```

## Tests

```bash
vendor/oak-linux-v0.1 lru.test.oak
```

## Benchmarks

```bash
vendor/oak-linux-v0.1 lru.bench.oak
```
