# Benchmark google-polyline

Comparing couple of implementations of a polyline encoding algorithm:
- [@pirxpilot/google-polyline](https://www.npmjs.com/package/@pirxpilot/google-polyline)
- [google-polyline (`jhermsmeier`)](https://www.npmjs.com/package/google-polyline)


_;tldr_ the `jhermsmeier` one is quicker, but uses `[lat, lng]` instead of GeoJSON's `[lng, lat]`


## Results

```
# @pirxpilot/google-polyline decode 1000 times
ok ~27 ms (0 s + 27117951 ns)

# @pirxpilot/google-polyline encode 1000 times
ok ~9.16 s (9 s + 160988585 ns)

# google-polyline decode 1000 times
ok ~16 ms (0 s + 15532722 ns)

# google-polyline encode 1000 times
ok ~567 ms (0 s + 566985141 ns)

all benchmarks completed
ok ~9.77 s (9 s + 770624399 ns)
```