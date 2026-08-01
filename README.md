# Abid Khan

> Building AI for the ones who can't build it for themselves — and shipping the software around it.

AI/ML & full-stack engineer. **GSoC 2026 @ NumFOCUS / scikit-bio**, where I make scientific-Python hot paths fast (Numba · Array API · GPU). Around that I build LLM tools and evaluations — much of it aimed at animal advocacy with **[Open Paws](https://www.openpaws.ai)** — and I merge code into projects people actually run.

I like reproducible benchmarks, honest negative results, and code that ships.

---

### 🧬 GSoC 2026 · scikit-bio (NumFOCUS)

Porting performance-critical Cython to **Numba**, with **Array-API / GPU-resident** paths for PERMANOVA, Mantel, and distance matrices — one source, CPU → GPU.

`10 merged PRs`  ·  `2.4× vs Cython` (n=3000)  ·  `<1e-15` numerical agreement

→ [scikit-bio/scikit-bio](https://github.com/scikit-bio/scikit-bio)

### 🧪 AI / ML

- **[inspect-speciesism-eval](https://github.com/LarytheLord/inspect-speciesism-eval)** — an LLM value-alignment evaluation on UK AISI's **Inspect** framework; it surfaces when a model *recognizes* a harm yet still rates it acceptable. Truncation-aware scorer built for reasoning models · 13 tests. (Ongoing research into the framing-robustness of moral judgment; cross-family replication in progress.)
- **Applied LLMs** — a production **RAG** system (Pinecone + OpenAI), LLM civic tooling, and RLHF data pipelines.

### 🔧 Open Source — merged code

Fixes and features merged into projects at real scale:

**[daytona](https://github.com/daytonaio/daytona/pull/4107)** ⭐72k · **[docling](https://github.com/docling-project/docling/pull/3134)** ⭐64k · **[helm](https://github.com/helm/helm/pull/31907)** ⭐30k · **[kubernetes](https://github.com/kubernetes/kubernetes/pull/137283)** · **[OpenHands](https://github.com/All-Hands-AI/OpenHands/pull/13471)**

<details><summary><b>Full merged-PR list (16, all authored & merged)</b></summary>

| Repo | PR | What |
|---|---|---|
| daytonaio/daytona ⭐72k | [#4107](https://github.com/daytonaio/daytona/pull/4107) | Stop sync session commands hanging on stdin |
| docling-project/docling ⭐64k | [#3134](https://github.com/docling-project/docling/pull/3134) | Fix image-backend resource leaks (unclosed PIL handles) |
| helm/helm ⭐30k | [#31907](https://github.com/helm/helm/pull/31907) | Hermetic User-Agent REST-config test |
| All-Hands-AI/OpenHands | [#13471](https://github.com/All-Hands-AI/OpenHands/pull/13471) | Treat `llm_base_url=""` as an explicit clear |
| kubernetes/kubernetes | [#137283](https://github.com/kubernetes/kubernetes/pull/137283) | Clarify `envFrom` env-var key constraints |
| scverse/scanpy | [#3986](https://github.com/scverse/scanpy/pull/3986) | Remove duplicated Louvain/Leiden docs |
| nextflow-io/nextflow | [#6869](https://github.com/nextflow-io/nextflow/pull/6869) | Clarify `Path.name` for staged inputs |
| mlco2/codecarbon | [#1080](https://github.com/mlco2/codecarbon/pull/1080) | Quiet tracebacks on auth/config failure |
| pyinat/pyinaturalist | [#682](https://github.com/pyinat/pyinaturalist/pull/682) · [#684](https://github.com/pyinat/pyinaturalist/pull/684) · [#686](https://github.com/pyinat/pyinaturalist/pull/686) · [#679](https://github.com/pyinat/pyinaturalist/pull/679) | Type-safe constants, annotation labels, docs |
| openfoodfacts/openfoodfacts-dart | [#1203](https://github.com/openfoodfacts/openfoodfacts-dart/pull/1203) | pub.dev package-score CI workflow |
| simonoppowa/OpenNutriTracker | [#304](https://github.com/simonoppowa/OpenNutriTracker/pull/304) (+#303/#305/#311) | Custom meals in search + onboarding fixes |
| sustainable-computing-io/kepler | [#2431](https://github.com/sustainable-computing-io/kepler/pull/2431) | Deploy without Prometheus Operator |
| gbif/pygbif | [#200](https://github.com/gbif/pygbif/pull/200) | Clarify auth env-vars for downloads |
| openfoodfacts/smooth-app | [#7427](https://github.com/openfoodfacts/smooth-app/pull/7427) | Align Flutter version refs |
| prometheus/docs | [#2855](https://github.com/prometheus/docs/pull/2855) | Update Pushgateway references |
| JuliaNeighbors/Neighborhood.jl | [#19](https://github.com/JuliaNeighbors/Neighborhood.jl/pull/19) | Docs wording fix |

*Open:* [biopython/biopython#5170](https://github.com/biopython/biopython/pull/5170).
</details>

### 🚀 Shipped

- **[Adventurers Guild](https://adventurersguild.space)** — gamified developer-project marketplace · Next.js · Prisma/Neon · Stripe · CI + tests
- **knight-medicare** — mental-health video-consultation platform · Next.js · Supabase · LiveKit · *CTO & co-founder*
- **[Open Permit](https://openpermit.vercel.app)** — LLM civic tool: monitors development permits, drafts cited objections · Gemini · Supabase
- **[AFA Resource Chatbot](https://afachatbot.vercel.app)** — production RAG over the Asia-for-Animals resource database · Pinecone · OpenAI
- **Material Innovation** — B2B sustainable-materials platform · Next.js · Supabase · Stripe

### 🧰 Stack

`Python` `TypeScript` `Go` `Julia` — Numba · NumPy · Array API · Inspect · transformers/trl · RAG
Next.js · React · FastAPI — PostgreSQL/Supabase · Docker · Vercel · GitHub Actions

📫 **llawlietbagsum@gmail.com**  ·  🌐 **[abikhn.vercel.app](https://abikhn.vercel.app/)**  ·  📊 **[Kaggle](https://www.kaggle.com/larythelord)**
