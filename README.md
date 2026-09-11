I build distributed ingestion services and the operational tooling around them.
## Paige Huels
I own APIs, queue consumers, and schema evolution from proposal through production. I keep data paths observable and design deployments that fail without losing work. I prefer boring boundaries, explicit contracts, and small reversible changes. The trade-off I accept is slower first passes when they make later operations safer.
### 🛠 Tech & Infrastructure
**Core** — `TypeScript`, `Node.js`, `PostgreSQL`, `Redis`
**Messaging** — `Apache Kafka`, `Rust`, `Apache Flink`
**Infra** — `Docker`, `Kubernetes`, `Terraform`
**Tooling** — `OpenTelemetry`, `Prometheus`, `GitHub Actions`
### ⚙️ Engineering Areas
- Designing Kafka consumer groups, checkpoints, and idempotent replay paths.
- Versioning event schemas with contract tests across producers and consumers.
- Tracing RPCs, queue latency, and worker saturation with OpenTelemetry.
- Running database migrations against snapshots before production rollout.
### 🔭 Current Focus
- Moving checkpoint writes from Redis to Kafka log offsets to remove a single node of state.
- Limiting consumer concurrency so one unhealthy partition cannot exhaust worker memory.
- Replaying captured traffic through contract tests without copying production payloads.
- Separating replay workers from serving workers to contain retry storms.
### 📌 Engineering Notes
- Tests should cover boundary conditions and failure injection, not only happy paths.
- Boundaries need explicit ownership, schemas, and error contracts.
- Migrations should be additive, reversible, and independently observable.
- Retries need bounded backoff, deadlines, and a reason to remain visible in traces.
### 🧭 How I Work
- Choose the smallest design that keeps failure modes inspectable.
- Prefer schemas and contracts that let services evolve independently.
- Treat operational evidence as part of a production change.
*Small, observable changes are easier to operate and safer to reverse.*
[Email](mailto:madeleinesabater1917758@gmail.com)