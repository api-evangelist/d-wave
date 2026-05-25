# D-Wave

D-Wave Quantum Inc. (NYSE: **QBTS**) is the leader in commercial quantum annealing computing
and the maker of the Advantage and Advantage2 quantum systems. The Leap quantum cloud
service provides real-time access to D-Wave QPUs and to the Leap hybrid solver family
(BQM, CQM, DQM, NL) capable of solving industrial optimization problems with up to
~2 million variables and constraints.

This is the API Evangelist catalog entry for D-Wave, profiling D-Wave's public developer
surface — the Solver API (SAPI), the Metadata API, the Leap Account API, the Leap hybrid
solvers, the QPU samplers, and the Ocean SDK ecosystem.

- Portal: https://www.dwavequantum.com
- Documentation: https://docs.dwavequantum.com/en/latest/
- Industrial Optimization: https://docs.dwavequantum.com/en/industrial_optimization/index_get_started.html
- Quantum Research: https://docs.dwavequantum.com/en/quantum_research/index_get_started.html
- Leap cloud: https://cloud.dwavesys.com/leap/
- GitHub orgs: [dwavesystems](https://github.com/dwavesystems) and [dwave-examples](https://github.com/dwave-examples)
- Investor relations: https://investor.dwavequantum.com (NYSE: QBTS)

## APIs

| API | Base URL | Description |
| --- | --- | --- |
| [SAPI Solvers](openapi/d-wave-solvers-api-openapi.yml) | `https://cloud.dwavesys.com/sapi/v2` | Discover, inspect, and filter solvers (QPU + hybrid). |
| [SAPI Problems](openapi/d-wave-problems-api-openapi.yml) | `https://cloud.dwavesys.com/sapi/v2` | Submit, monitor, retrieve, cancel problem jobs. |
| [Metadata API](openapi/d-wave-metadata-api-openapi.yml) | `https://api.dwavesys.com/metadata/v1` | Region discovery and per-region SAPI endpoints. |
| [Leap Account API](openapi/d-wave-leap-account-api-openapi.yml) | `https://cloud.dwavesys.com/leap/api` | OAuth-backed project / SAPI-token management. |
| [Hybrid Solvers](openapi/d-wave-hybrid-solvers-openapi.yml) | `https://cloud.dwavesys.com/sapi/v2` | BQM, CQM, DQM, NL hybrid solver submission. |
| [QPU Samplers](openapi/d-wave-qpu-samplers-openapi.yml) | `https://cloud.dwavesys.com/sapi/v2` | Direct Ising / QUBO sampling on Advantage / Advantage2 QPUs. |

## Authentication

- **SAPI (Solver / Problems / Metadata)** — opaque project SAPI token sent as the
  `X-Auth-Token` header, e.g. `DEV-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`.
- **Leap Account API** — OAuth 2.0 authorization code flow against
  `https://cloud.dwavesys.com/leap/oauth/` to retrieve user account, projects, and
  per-project SAPI tokens.

## Problem Types & Encoding

D-Wave's six canonical problem types — `ising`, `qubo`, `bqm`, `cqm`, `dqm`, `nl` — are
submitted with one of three encoding formats: `qp` (compact QPU encoding), `bq` (dimod
serialized model), or `ref` (external binary reference downloaded with SAPI-token auth).

Problem lifecycle: `PENDING` → `IN_PROGRESS` → `COMPLETED` | `FAILED` | `CANCELLED`
(terminal). Batch status polls accept up to 1,000 problem IDs.

## Ocean SDK

D-Wave's developer experience is anchored by the open-source Ocean SDK:

- [`dwave-ocean-sdk`](https://github.com/dwavesystems/dwave-ocean-sdk) — meta-installer
- [`dimod`](https://github.com/dwavesystems/dimod) — shared QUBO / Ising / CQM / DQM / NL data model
- [`dwave-system`](https://github.com/dwavesystems/dwave-system) — DWaveSampler, EmbeddingComposite, LeapHybridSampler
- [`dwave-cloud-client`](https://github.com/dwavesystems/dwave-cloud-client) — SAPI REST client
- [`dwave-hybrid`](https://github.com/dwavesystems/dwave-hybrid) — async decomposition framework
- [`dwave-samplers`](https://github.com/dwavesystems/dwave-samplers) — classical reference solvers
- [`dwave-optimization`](https://github.com/dwavesystems/dwave-optimization) — C++ NL engine
- [`dwave-preprocessing`](https://github.com/dwavesystems/dwave-preprocessing)
- [`dwave-inspector`](https://github.com/dwavesystems/dwave-inspector) — interactive problem inspector
- [`minorminer`](https://github.com/dwavesystems/minorminer) — minor-embedding heuristic
- [`dwave-graphs`](https://github.com/dwavesystems/dwave-graphs) — Pegasus / Zephyr / Chimera graphs
- [`dwave-gate`](https://github.com/dwavesystems/dwave-gate) — gate-model simulator
- [`dwave-pytorch-plugin`](https://github.com/dwavesystems/dwave-pytorch-plugin),
  [`dwave-scikit-learn-plugin`](https://github.com/dwavesystems/dwave-scikit-learn-plugin),
  [`dwave-qiskit-plugin`](https://github.com/dwavesystems/dwave-qiskit-plugin)

60+ reference applications live at [github.com/dwave-examples](https://github.com/dwave-examples).

## Artifacts

- **OpenAPI** — `openapi/`
- **JSON Schema** — `json-schema/` (solver configuration, problem job, problem answer, CQM, QPU properties)
- **JSON-LD context** — [`json-ld/d-wave-context.jsonld`](json-ld/d-wave-context.jsonld)
- **Examples** — `examples/` (list solvers, submit problem, problem status, regions, Leap projects, CQM, QPU Ising)
- **Naftiko capabilities** — `capabilities/` (solver discovery, problem submission, monitoring, regions, account, hybrid CQM/NL, QPU sampling)
- **Vocabulary** — [`vocabulary/d-wave-vocabulary.yml`](vocabulary/d-wave-vocabulary.yml)
- **Spectral rules** — [`rules/d-wave-rules.yml`](rules/d-wave-rules.yml)
- **Plans** — [`plans/d-wave-plans-pricing.yml`](plans/d-wave-plans-pricing.yml)
- **Rate Limits** — [`rate-limits/d-wave-rate-limits.yml`](rate-limits/d-wave-rate-limits.yml)
- **FinOps** — [`finops/d-wave-finops.yml`](finops/d-wave-finops.yml)

## License

Profile content is published under the same terms as the rest of api-evangelist; the
underlying Ocean SDK is open source under Apache-2.0.
