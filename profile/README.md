# CacheConnections

CacheConnections aims to be a cross-language, high-performance caching library offering diverse caching strategies tailored to various use cases and workflows. The project currently supports .NET with plans to expand to Rust and Go in the future.

## Features

- Thread-Safe Cache Implementations
- Extensible Architecture
- Multiple Caching Strategies (in-progress):
- [X] LRU (Least Recently Used) Cache (available in .NET)
- [ ] Additional strategies like MRU, LFU, ARC, etc., coming soon

Comprehensive Benchmarking Tools
Support for Modern Frameworks
- .NET 9.0 (current)
- Rust and Go (future targets)

## Quick Start (.NET)
```
using Cache.Caches;

// Create a new LRU cache with a capacity of 1000 items
var cache = new LruCache<string, string>(capacity: 1000);

// Add items
cache.Put("key1", "value1");

// Retrieve items
string? value = cache.Get("key1");
```

## Performance

Benchmarks included for:
- Single-threaded operations
- Concurrenct access patterns
- Eviction scenarios
- High-contention workloads

Running benchmarks for .NET
```
cd dotnet/benchmarks/Cache.Benchmarks
dotnet run -c Release
```

## Roadmap
1. Expand .NET Cache Implementations
- Most Recently Used (MRU)
- Least Frequently Used (LFU)
- Time-Based Expiration
- Adaptive Replacement Cache (ARC)
- Two-Queue Cache (2Q)
- TinyLFU, SLRU, and Clock Cache

2. Rust and Go Implementations
- Port LRU
- Add other caching strategies

3. Advanced Features
- Distributed cache support
- Hybrid/multi-tier cache strategies
- Cache persistence
- Statistics and monitoring tools
- Event notifications for cache operations
- Plug-and-play architecture for custom policies

## Contributions
**Contributions are welcome! Here’s how you can help:**
1. Fork the repository
2. Create a feature branch:
```git checkout -b feature/amazing-feature```
3. Commit your changes:
```git commit -m 'Add some amazing feature'```
4. Push to the branch:
```git push origin feature/amazing-feature```
5. Open a pull request
**Areas for Contribution:**
- Cache implementation (For now additional .NET strategies)
- Performance optimizations
- Documentation and examples
- Bug fixes and tests
##  License
This project is licensed under the MIT License.
