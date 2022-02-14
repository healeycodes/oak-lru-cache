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

## Tests

```bash
vendor/oak-linux-v0.1 lru.test.oak
```

## Benchmarks

```bash
vendor/oak-linux-v0.1 lru.bench.oak
```
