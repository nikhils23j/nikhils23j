# Hi, I'm Nikhil Jain 👋

**Quant, Systems, and machine learning** · B.Tech in Electrical Engineering, IIT Kanpur (2026) · Bengaluru, India

I enjoy working close to the systems that make software reliable: Linux, networks, production infrastructure, and performance-sensitive code. My experience includes infrastructure support at **Squarepoint Capital** and wireless modem analytics at **Samsung R&D**. Outside work, I build projects across networking, developer tools, and applied ML.

[Portfolio](https://nikhilj22.vercel.app) · [LinkedIn](https://linkedin.com/in/nikhil-jain-907100253) · [Codeforces](https://codeforces.com/profile/nikhilj22.iitk) · [Email](mailto:nikhilj22.iitk@gmail.com)

## What I've worked on

- **Production infrastructure:** Investigated Linux, Kubernetes, compute, storage, and networking incidents supporting global trading and research environments at Squarepoint Capital.
- **Wireless + ML:** Used modem logs and XGBoost to study LTE/5G link adaptation and modulation and coding scheme prediction during my Samsung R&D internship.
- **Systems research:** Worked on GPU Direct TCP, a course research prototype that moves network packets directly into GPU memory for GPU-side TCP processing.
- **Community:** Served as a Google Developer Groups campus organiser and as a manager in IIT Kanpur's Academic and Career Council.

## Featured projects
Every number below comes from a saved results file in the repo, and each README has a "what the numbers do NOT show" section.

### Latest additions

| Project | Focus | Measured result and scope |
| --- | --- | --- |
| [TraceGuard](https://github.com/nikhils23j/traceguard-replayable-tool-agent) | Replayable local tool-use agent with a deterministic authority gate and crash-safe writes | 144/144 guarded outcomes on a fixed synthetic 48-task × 3-seed suite; 20/20 injected post-commit restarts reached correct state |
| [FieldBridge](https://github.com/nikhils23j/fieldbridge-shadow-replay) | Shadow-replayed integration cutover with approval and rollback | 120,000 logical events across 120 local synthetic runs; zero valid events unapplied against an independent reference |

<p align="center">
  <a href="https://github.com/nikhils23j/worldquant-labs/tree/main/exchangelab"><img src="https://raw.githubusercontent.com/nikhils23j/worldquant-labs/main/docs/img/exchange_latency_cliff.png" width="49%" alt="ExchangeLab: arb PnL vs probe latency"></a>
  <a href="https://github.com/nikhils23j/incidentops"><img src="https://raw.githubusercontent.com/nikhils23j/incidentops/main/docs/img/dashboard.png" width="49%" alt="IncidentOps live dashboard"></a>
</p>

### Quant & market microstructure

| Project | What it explores | Headline result |
| --- | --- | --- |
| [ExchangeLab](https://github.com/nikhils23j/worldquant-labs/tree/main/exchangelab) | Price-time matching engine plus a microsecond agent market: does being 50 µs slower cost you anything? | Latency cost is a cliff: 20→70 µs cut a stale-quote arb's PnL by 44% against a 50 µs rival; engine matched a reference on 1.6M orders |
| [RiskLab](https://github.com/nikhils23j/worldquant-labs/tree/main/risklab) | Monte Carlo option pricing: QMC, variance reduction, Greeks, barriers, Heston | Sobol + Brownian bridge + control variate: ~17,000× variance reduction on an Asian option |
| [Market Data Replay](https://github.com/nikhils23j/market-data-replay) | C++20 binary order-by-order feed with A/B line arbitration, snapshot recovery and an SPSC pipeline | Bitmap book at 42.2M msg/s (2.1× `std::map`); 3.2M-event differential fuzz with 0 mismatches |
| [False-Discovery Alpha Lab](https://github.com/nikhils23j/false-discovery-alpha-screening-lab) | How many backtested "alphas" are luck? 217 formulas over 610 simulated markets | BH false-discovery rate was 15.2% with iid p-values vs 5.8% with 50-day block permutations |

### Systems & infrastructure

| Project | What it explores | Headline result |
| --- | --- | --- |
| [Fleet Config Consistency](https://github.com/nikhils23j/fleet-configuration-consistency) | Two-phase config rollout with leases and fencing tokens, chaos-tested on a deterministic simulator and real sockets | 0 of 55,015 reads saw mixed versions across 500 fault schedules; rolling/canary push mixed versions in every run |
| [K8s Recovery Operator](https://github.com/nikhils23j/inference-deployment-recovery-operator) | Python Kubernetes operator: watch cache, backoff queue, Lease leader election, automatic image rollback | v1 repaired 30/30 faults on k3s in ≤0.869 s; v2 converged in 300/300 simulated chaos schedules |
| [LLM-Serving Scheduler](https://github.com/nikhils23j/local-rpc-inference-transport) | C++ gRPC token streaming with continuous batching, priority lanes and admission control (synthetic compute) | p99 time-to-first-token 28 ms vs 265 ms for static batching at equal throughput |
| [GPU Cluster Scheduler Sim](https://github.com/nikhils23j/multi-tenant-gpu-placement-simulator) | 256-GPU cluster with MIG slices, NVLink islands, gang scheduling, preemption and failures; 7 policies | EASY reservations cut the worst big-job wait from 297 h to 82 h vs greedy backfill |
| [GPU Direct TCP](https://github.com/nikhils23j/GPU-direct-TCP) | GPU-resident TCP/IP processing and direct NIC-to-GPU packet transfer in a research prototype | Course research prototype |

### Verification, testing & apps

| Project | What it explores | Headline result |
| --- | --- | --- |
| [GPU Pipeline Verification](https://github.com/nikhils23j/gpu-command-pipeline-ip-verification) | SystemVerilog ALU pipeline with a reorder buffer, verified with SV + cocotb testbenches | All 9 injected RTL bugs caught; 227,699 outputs checked, 174/174 coverage bins |
| [API Authorization Lab](https://github.com/nikhils23j/api-contract-authorization-regression) | Multi-tenant API checked against a reference model with stateful random testing and shrinking | Caught 30/30 seeded authz bugs vs 24 for request enumeration; failures shrink to 1–3 step repros |
| [IncidentOps](https://github.com/nikhils23j/incidentops) | Spring Boot + React incident tracker with SLA escalation, live SSE updates and optimistic locking | In an 8-way simultaneous-ack race exactly 1 wins (6 without locking); 45 + 17 tests |
| [Sniff.in](https://github.com/nikhils23j/sniff.in) | A campus social app with mobile clients, a Supabase backend, and an invite website | |

## Tech stack

| Area | Tools and technologies I've used |
| --- | --- |
| **Languages** | C++, C, Python, Java, TypeScript, SQL, Bash, SystemVerilog |
| **Systems & infrastructure** | Linux, Docker, Kubernetes, Git, SSH, Slurm, Prometheus, Grafana, gRPC/Protobuf |
| **Networking** | TCP/IP, DNS, sockets, NICs, network troubleshooting |
| **Web & data** | React, Spring Boot, Supabase, PostgreSQL, Redis |
| **Machine learning** | XGBoost, NLP, transformers, model evaluation |
| **Quant & simulation** | NumPy, SciPy, QuantLib, Monte Carlo/QMC, discrete-event simulation |
| **Verification & testing** | Icarus Verilog, cocotb, property/stateful testing, differential fuzzing, sanitizers |

## Beyond the code

- 🎓 IIT Kanpur, Electrical Engineering; minors in Computer Systems, Machine Learning, and Algorithms.
- 🧩 Codeforces **Expert**: [nikhilj22.iitk](https://codeforces.com/profile/nikhilj22.iitk).
- 📫 Reach me at **[nikhilj22.iitk@gmail.com](mailto:nikhilj22.iitk@gmail.com)** or connect on [LinkedIn](https://linkedin.com/in/nikhil-jain-907100253).
