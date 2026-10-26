# D-Wave (d-wave)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

D-Wave Quantum Inc. (NYSE: QBTS) is the leader in commercial quantum annealing computing and developer of the Advantage and Advantage2 quantum systems. D-Wave's Leap quantum cloud service provides real-time access to D-Wave QPUs and to the Leap hybrid solver family (BQM, CQM, DQM, NL) capable of solving industrial optimization problems with up to ~2 million variables and constraints. The open-source Ocean SDK — dimod, dwave-system, dwave-cloud-client, dwave-hybrid, dwave-samplers, dwave-optimization, minorminer, dwave-inspector, and 40+ companion packages — provides the canonical developer experience, with the underlying Solver API (SAPI) exposed as a versioned REST interface for solver discovery, problem submission, status polling, answer retrieval, and cancellation. Companion APIs include the Metadata API for region discovery and the Leap Account API for OAuth-based project and token management.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/d-wave/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/d-wave/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Quantum Computing
- Quantum Annealing
- Optimization
- Hybrid Quantum-Classical
- Ising
- QUBO
- Industrial Optimization
- Sampling
- Leap
- Ocean SDK
- SAPI

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### D-Wave Solver API (SAPI) - Solvers

List, inspect, and discover D-Wave solvers available to the authenticated project, including quantum annealing QPU samplers (Advantage, Advantage2) and Leap hybrid samplers (BQM, CQM, DQM, NL). Solvers carry capability metadata (qubit count, topology, supported problem types, parameters, properties) so clients can match a workload to the correct sampler. Versioned via vendor media type `application/vnd.dwave.sapi.solver-definition+json;version~=3.0`.

- **Human URL:** [https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html](https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html)
- **Base URL:** `https://cloud.dwavesys.com/sapi/v2`

#### Tags

- Quantum Computing
- Quantum Annealing
- Solvers
- Optimization

#### Properties

- [Documentation](https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html)
- [OpenAPI](openapi/d-wave-solvers-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-wave-solvers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-wave-solvers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/d-wave-solver-configuration-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/d-wave-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/d-wave-list-solvers-example.json)

### D-Wave Solver API (SAPI) - Problems

Submit, monitor, retrieve, and cancel quantum and hybrid problem jobs. Supports the canonical problem types ising, qubo, bqm, cqm, dqm, and nl with three encoding formats (qp, bq, ref). Problems flow through PENDING > IN_PROGRESS > COMPLETED | FAILED | CANCELLED terminal states. Endpoints support blocking submit (single problem), batch async submit (multi-problem), short status polling, full-info retrieval, answer download (inline or binary-ref via SAPI-token), problem messages, and single/bulk cancel. Up to 1,000 problem IDs per status batch.

- **Human URL:** [https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html](https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html)
- **Base URL:** `https://cloud.dwavesys.com/sapi/v2`

#### Tags

- Quantum Computing
- Quantum Annealing
- Problems
- Sampling
- Optimization

#### Properties

- [Documentation](https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html)
- [OpenAPI](openapi/d-wave-problems-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-wave-problems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-wave-problems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/d-wave-problem-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/d-wave-problem-answer-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/d-wave-submit-problem-example.json)
- [Example](examples/d-wave-problem-status-example.json)

### D-Wave Metadata API - Regions

Discover D-Wave Leap regions and their per-region SAPI endpoints. The Metadata API is the canonical region resolver — clients call `/regions/` to enumerate available regions (e.g. `na-west-1`, `eu-central-1`) and `/regions/{code}` to retrieve a single region's SAPI base URL. Used by the Ocean `dwave-cloud-client` to route problem submissions to the correct regional SAPI cluster. Versioned via `application/vnd.dwave.metadata.regions+json;version~=1.0`.

- **Human URL:** [https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html](https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html)
- **Base URL:** `https://api.dwavesys.com/metadata/v1`

#### Tags

- Quantum Computing
- Metadata
- Regions

#### Properties

- [Documentation](https://docs.dwavequantum.com/en/latest/ocean/api_ref_cloud/index.html)
- [OpenAPI](openapi/d-wave-metadata-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-wave-metadata-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-wave-metadata-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/d-wave-list-regions-example.json)

### D-Wave Leap Account API

Manage Leap account projects and per-project SAPI tokens via OAuth. Endpoints include `account/active_project/oauth/` (retrieve user's active project), `account/projects/oauth/` (list all accessible projects), and `account/token/oauth/?project_id=...` (retrieve a project SAPI token for use against the Solver API). Backs the Ocean SDK's interactive Leap authorization flow, allowing developers to onboard, switch projects, and rotate SAPI tokens without leaving their development environment.

- **Human URL:** [https://docs.dwavequantum.com/en/latest/leap_sapi/leap_api.html](https://docs.dwavequantum.com/en/latest/leap_sapi/leap_api.html)
- **Base URL:** `https://cloud.dwavesys.com/leap/api`

#### Tags

- Quantum Computing
- Leap
- Account
- Projects
- OAuth

#### Properties

- [Documentation](https://docs.dwavequantum.com/en/latest/leap_sapi/leap_api.html)
- [OpenAPI](openapi/d-wave-leap-account-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-wave-leap-account-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-wave-leap-account-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/d-wave-leap-projects-example.json)

### D-Wave Leap Hybrid Solvers

Quantum-classical hybrid solvers accessible via SAPI. Five hybrid solver families — BQM (binary quadratic), CQM (constrained quadratic, supports equality/inequality constraints), DQM (discrete quadratic), NL (nonlinear, the Industrial Optimization workhorse) — plus the LeapHybridSampler family. Supports industry-scale problems up to ~2 million variables and constraints; subsecond response times for smaller problems. Submitted as standard SAPI problems with `type=cqm|bqm|dqm|nl` and the relevant solver name.

- **Human URL:** [https://docs.dwavequantum.com/en/industrial_optimization/index_get_started.html](https://docs.dwavequantum.com/en/industrial_optimization/index_get_started.html)
- **Base URL:** `https://cloud.dwavesys.com/sapi/v2`

#### Tags

- Quantum Computing
- Hybrid
- Optimization
- BQM
- CQM
- DQM
- Nonlinear

#### Properties

- [Documentation](https://docs.dwavequantum.com/en/industrial_optimization/index_get_started.html)
- [OpenAPI](openapi/d-wave-hybrid-solvers-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-wave-hybrid-solvers.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-wave-hybrid-solvers.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/d-wave-cqm-model-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/d-wave-cqm-problem-example.json)

### D-Wave QPU Samplers (Advantage / Advantage2)

Direct access to D-Wave quantum annealing QPUs — Advantage (5,000+ qubits, Pegasus topology) and Advantage2 (next-generation, Zephyr topology). Submit Ising or QUBO problems with parameters for annealing schedule, num_reads, chain_strength, reverse annealing, h_gain_schedule, programming thermalization, and readout thermalization. Returned answers contain energies, occurrences, and sample vectors. Use DWaveSampler/EmbeddingComposite from `dwave-system` to embed logical problems onto the physical qubit graph.

- **Human URL:** [https://docs.dwavequantum.com/en/quantum_research/index_about.html](https://docs.dwavequantum.com/en/quantum_research/index_about.html)
- **Base URL:** `https://cloud.dwavesys.com/sapi/v2`

#### Tags

- Quantum Computing
- Quantum Annealing
- QPU
- Advantage
- Advantage2
- Pegasus
- Zephyr

#### Properties

- [Documentation](https://docs.dwavequantum.com/en/quantum_research/index_about.html)
- [OpenAPI](openapi/d-wave-qpu-samplers-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-wave-qpu-samplers.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-wave-qpu-samplers.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/d-wave-qpu-properties-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/d-wave-qpu-ising-example.json)

## Common Properties

- [Portal](https://www.dwavequantum.com)
- [Documentation](https://docs.dwavequantum.com/en/latest/)
- [Documentation](https://docs.dwavequantum.com/en/industrial_optimization/index_get_started.html)
- [Documentation](https://docs.dwavequantum.com/en/quantum_research/index_get_started.html)
- [Documentation](https://docs.dwavequantum.com/en/concepts/index.html)
- [Getting Started](https://www.dwavequantum.com/build/getting-started/)
- [Sign Up](https://www.dwavequantum.com/get-started-with-d-wave/)
- [Sign Up](https://cloud.dwavesys.com/leap/signup/)
- [Sandbox](https://cloud.dwavesys.com/leap/)
- [GitHub Organization](https://github.com/dwavesystems)
- [GitHub Organization](https://github.com/dwave-examples)
- [SDK](https://github.com/dwavesystems/dwave-ocean-sdk)
- [SDK](https://github.com/dwavesystems/dwave-cloud-client)
- [SDK](https://github.com/dwavesystems/dwave-system)
- [SDK](https://github.com/dwavesystems/dimod)
- [SDK](https://github.com/dwavesystems/dwave-hybrid)
- [SDK](https://github.com/dwavesystems/dwave-samplers)
- [SDK](https://github.com/dwavesystems/dwave-optimization)
- [SDK](https://github.com/dwavesystems/dwave-neal)
- [SDK](https://github.com/dwavesystems/dwave-tabu)
- [SDK](https://github.com/dwavesystems/dwave-greedy)
- [SDK](https://github.com/dwavesystems/dwave-preprocessing)
- [Tool](https://github.com/dwavesystems/dwave-inspector)
- [SDK](https://github.com/dwavesystems/minorminer)
- [SDK](https://github.com/dwavesystems/dwave-graphs)
- [SDK](https://github.com/dwavesystems/dwave-gate)
- [SDK](https://github.com/dwavesystems/penaltymodel)
- [Plugins](https://github.com/dwavesystems/dwave-pytorch-plugin)
- [Plugins](https://github.com/dwavesystems/dwave-scikit-learn-plugin)
- [Plugins](https://github.com/dwavesystems/dwave-qiskit-plugin)
- [Tool](https://github.com/dwavesystems/ocean-docker)
- [Tool](https://github.com/dwavesystems/ocean-devcontainer)
- [Documentation](https://github.com/dwavesystems/leapide-docs)
- [Code Examples](https://github.com/dwave-examples)
- [Code Examples](https://github.com/dwave-examples/template)
- [Code Examples](https://github.com/dwave-examples/simple-ocean-programs)
- [Code Examples](https://github.com/dwave-examples/hybrid-computing-notebook)
- [Code Examples](https://github.com/dwave-examples/pegasus-notebook)
- [Code Examples](https://github.com/dwave-examples/reverse-annealing-notebook)
- [Code Examples](https://github.com/dwave-examples/factoring-notebook)
- [Code Examples](https://github.com/dwave-examples/feature-selection-notebook)
- [SDK](https://pypi.org/project/dwave-ocean-sdk/)
- [SDK](https://pypi.org/project/dwave-cloud-client/)
- [SDK](https://pypi.org/project/dwave-system/)
- [SDK](https://pypi.org/project/dimod/)
- [Portal](https://www.dwavequantum.com/solutions-and-products/cloud-platform/)
- [Portal](https://www.dwavequantum.com/solutions-and-products/systems/)
- [Portal](https://www.dwavequantum.com/solutions-and-products/professional-services/)
- [Blog](https://www.dwavequantum.com/learn/blog/)
- [Documentation](https://www.dwavequantum.com/learn/resource-library/)
- [Documentation](https://www.dwavequantum.com/learn/featured-applications/)
- [Forum](https://support.dwavesys.com/hc/en-us/community/topics)
- [Support](https://support.dwavesys.com/hc/en-us)
- [Support](https://www.dwavequantum.com/contact-us/)
- [Privacy Policy](https://www.dwavequantum.com/legal/privacy-policy/)
- [Terms of Service](https://www.dwavequantum.com/legal/terms/)
- [Documentation](https://www.dwavequantum.com/legal/patent-notice/)
- [Documentation](https://investor.dwavequantum.com)
- [LinkedIn](https://www.linkedin.com/company/d-wave-systems)
- [Twitter](https://x.com/dwavequantum)
- [YouTube](https://www.youtube.com/@dwavequantum)
- [Plans](https://plans/d-wave-plans-pricing.yml)
- [Rate Limits](https://rate-limits/d-wave-rate-limits.yml)
- [Fin Ops](https://finops/d-wave-finops.yml)
- [Vocabulary](vocabulary/d-wave-vocabulary.yml)
- [Spectral Rules](rules/d-wave-rules.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
