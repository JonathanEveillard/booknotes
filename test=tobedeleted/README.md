# Back-of-the-Envelope Estimation

> Book: System Design Interview | Chapter 2

## Key Concepts

Estimation is about getting a rough sense of scale before designing a system.
Always clarify assumptions with your interviewer upfront.

## Powers of Two

| Power | Approx Value | Full Name |
|-------|-------------|-----------|
| 10    | 1 thousand  | 1 KB      |
| 20    | 1 million   | 1 MB      |
| 30    | 1 billion   | 1 GB      |

## Latency Numbers to Know

- Memory access: ~100 ns
- SSD read: ~100 µs
- Network round trip (same region): ~500 µs

## Example Estimation: Twitter QPS

- 300M monthly active users
- 50% use daily → 150M DAU
- Average 2 tweets/day → **300M writes/day**
- QPS = 300M / 86400 ≈ **~3500 QPS**

## My Takeaways

- Always convert to per-second metrics early
- Storage and bandwidth are often the bottlenecks, not compute

## Related Notes

- [Chapter 1 - Scale from Zero to Millions](../ch01/README.md)
- [CAP Theorem](../../concepts/cap-theorem.md)
- [Latency Cheat Sheet](../../concepts/latency)