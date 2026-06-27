<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Space+Grotesk&weight=700&size=30&duration=2800&pause=900&color=A78BFA&center=true&vCenter=true&width=650&lines=Ayush+Ranjan;full+stack+dev+%C3%97+builder;go+%C2%B7+typescript+%C2%B7+flutter;new+delhi+%C2%B7+omniful+ai" alt="Ayush Ranjan" />

<br/>

<sub><code>new delhi &nbsp;·&nbsp; omniful ai &nbsp;·&nbsp; building things that matter</code></sub>

<br/><br/>

[![Discord](https://img.shields.io/badge/Discord-%235865F2.svg?style=flat-square&logo=discord&logoColor=white)](https://discord.com/users/753159553649999914)
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/ayusssshhhhhh_/)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=flat-square&logo=twitter&logoColor=white)](https://x.com/Ayuuuu_25)
[![Medium](https://img.shields.io/badge/Medium-%23000000.svg?style=flat-square&logo=medium&logoColor=white)](https://medium.com/@ranaayush0730)
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@TheComicConnection)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230A66C2.svg?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ayush-ranjan019/)
[![Portfolio](https://img.shields.io/badge/Portfolio-%23A78BFA.svg?style=flat-square&logo=vercel&logoColor=white)](https://ayuuu-pro.vercel.app/)

</div>

---

<div align="center">
  <img src="techstack.svg" alt="Tech Stack" />
</div>

---

```python
class Ayush:
    location     = "New Delhi, India"
    current_role = "SDE @ Omniful AI"
    building     = ["high-throughput systems in Go", "distributed event pipelines", "AI-native tooling"]
    learning     = ["Rust", "eBPF", "consensus algorithms"]
    philosophy   = "if it's not fast, it's not done"
    interests    = ["system design", "compilers", "low-level networking", "comic books", "gaming"]
    ask_me_about = ["Go internals", "event-driven architecture", "why Dart is underrated"]

    def available_for(self):
        return ["collabs", "open source", "side projects", "coffee chats"]
```

---

```
// currently shipping

▶  qcache          — in-memory KV store, custom eviction, Redis RESP protocol    [ Go           ]  ████████░░  80%
▶  event_arcade    — distributed arcade engine, Kafka-backed event bus           [ TypeScript   ]  █████░░░░░  55%
▶  prepio          — interview prep platform, Go microservices + Flutter         [ Next/Flutter ]  ███░░░░░░░  30%

// on the radar

○  Rust            — ownership model, zero-cost abstractions, WASM target
○  eBPF            — kernel-level observability without instrumentation overhead
○  WebAssembly     — portable, sandboxed, near-native execution in the browser
```

---

### event_arcade

A distributed arcade battle engine built for scale. The core challenge: simulate hundreds of concurrent player sessions with deterministic outcomes, zero state drift across nodes, and a tamper-evident audit trail.

```
architecture

  clients ──► WebSocket gateway ──► Kafka topic (battle-events)
                                         │
                              ┌──────────┼──────────┐
                              ▼          ▼          ▼
                         worker-0    worker-1    worker-N
                              │          │          │
                         append-only JSONL log (per-session)
                              │
                         Redis (leaderboard, session cache)
                              │
                         SHA-256 chain (integrity verification)
```

```
key design decisions

  deterministic matchmaking   →  seeded RNG, reproducible outcomes from same input sequence
  single-writer log           →  one goroutine owns each session log, eliminates write contention
  Kafka partitioning          →  partition by session-id, preserves per-session event ordering
  Redis sorted sets           →  O(log N) leaderboard ops, TTL-based session expiry
  integrity chain             →  each log entry hashes prev_hash + payload, detect any tampering
  worker pool                 →  goroutine-per-session model, back-pressure via channel buffers
```

> scaling target: 10k concurrent sessions, sub-5ms matchmaking, full audit trail, horizontally scalable workers

---

<div align="center">
<sub>always down to collab &nbsp;·&nbsp; <a href="mailto:ranaayush0725@gmail.com">ranaayush0725@gmail.com</a></sub>
</div>
