# Abid Khan

Computer engineering undergraduate (graduating 2028). I make scientific Python fast and portable (Numba, Array API, GPU), and I evaluate LLMs, including when my own results turn out wrong.

I like reproducible benchmarks, honest negative results, and code that ships.

---

### Google Summer of Code 2026: scikit-bio (NumFOCUS), completed

Numba and Array API project, 350 hours, mentored by Dr. Igor Sfiligoi (San Diego Supercomputer Center). I ported performance-critical Cython to Numba and added GPU paths for PERMANOVA, Mantel and PERMDISP, so the same code runs on NumPy, CuPy, JAX and PyTorch.

- **34 merged PRs in scikit-bio**, 20 May to 22 Nov 2026. [All of them](https://github.com/scikit-bio/scikit-bio/pulls?q=is:pr+author:LarytheLord+is:merged).
- **Released in 0.7.4 (21 Sep 2026):** Numba engines for PERMANOVA, Mantel, PERMDISP and PCoA, `engine="fast"` for UniFrac, and GPU PERMANOVA and Mantel on NVIDIA and AMD ([release notes](https://github.com/scikit-bio/scikit-bio/releases/tag/0.7.4)). GPU PERMDISP and the condensed-matrix fixes are merged on main and not yet in a release.
- **One AMD MI300X, 25,000 samples, 9,999 permutations:** PERMANOVA took 426 s with the existing Cython code, 30 s with the Numba CPU engine and 7.3 s with the GPU kernel. Mantel took 1,407 s versus 157 s. p-values match Cython on MI210 and MI300X ([#2511](https://github.com/scikit-bio/scikit-bio/pull/2511)). Single machine; tables are in the PR.
- **Numba PERMDISP** is about 10x (centroid test) to 44x (median test) faster than Cython on 5,116-sample Earth Microbiome Project matrices, on 128 cores. It is still 4x to 6.6x on one thread, so most of the gain is removed Python overhead, not parallelism ([#2547](https://github.com/scikit-bio/scikit-bio/pull/2547)).
- Bugs found by testing on real hardware: float32 accumulation error in PERMANOVA (#2509), GPU-only failures in the Array API paths (#2530), a PERMDISP seed that never reached PCoA (#2546).

[![XERJ Corpus Hub contributor](https://hub.xerj.org/contributors/LarytheLord/badge.svg)](https://hub.xerj.org/contributors/LarytheLord) My permdisp GPU kernel was selected for the XERJ Corpus Hub, an open reference that AI coding agents search before writing code.

### LLM evaluation

- **[values-laundering](https://github.com/LarytheLord/values-laundering):** do LLM judges keep a moral verdict when only the wording of an act changes? 81 acts, six rewrite moves, ten judge families from seven labs. Pre-declared controls overturned my own headline result, and the repository reports that. A ranking found on older models did not hold on 2026 models; the effect itself persisted. Working paper, revision in progress after reviews at NeurIPS 2026 workshops, not accepted. [Dataset (CC-BY-4.0)](https://huggingface.co/datasets/LarytheLord/values-laundering).
- **[same-facts-softer-words](https://github.com/LarytheLord/same-facts-softer-words):** Apart Research sprint, Nov 2026. 11 real incidents from regulator records, six LLM judges. Company statements kept 10 to 40% of the regulator's core facts, and most of the score gap came from missing facts, not wording. Eleven incidents and six judges, so a small study.
- **[inspect-speciesism-eval](https://github.com/LarytheLord/inspect-speciesism-eval):** a 106-item evaluation on UK AISI's Inspect framework. My submission to the inspect_evals registry (#2056) was closed unmerged on a corpus-licensing policy; a docs fix to the same repo (#1978) was merged.
- **Global Open-source AI Challenge 2026 (Hangzhou):** one of 20 semifinalists in the AI for Research track, defended live to a panel in Sept 2026. Did not advance to the final.

### Open source

**69 merged PRs in 27 open-source projects run by other people** (as of 25 Nov 2026), 34 of them in scikit-bio. The other 35 are in 26 projects; 22 of those 35 are docs fixes and 12 change 10 lines or fewer. I left out PRs in hackathon and team repos that I or teammates merged. A few are bug fixes: a hung stdin in Daytona, a resource leak in Docling.

[Daytona](https://github.com/daytonaio/daytona/pull/4107) | [Docling](https://github.com/docling-project/docling/pull/3134) | [Helm](https://github.com/helm/helm/pull/31907) | [Kubernetes](https://github.com/kubernetes/kubernetes/pull/137283) | [OpenHands](https://github.com/All-Hands-AI/OpenHands/pull/13471) | Nextflow | scanpy | pyinaturalist | pygbif | codecarbon

Verify: [merged PRs by author, outside my own repos, includes team repos](https://github.com/search?q=author%3ALarytheLord+is%3Apr+is%3Amerged+-user%3ALarytheLord&type=pullrequests)

### Built

- **[Adventurers Guild](https://www.guilds.work):** developer marketplace that turns task requests into scoped work units with multi-agent QA review. Next.js, Prisma, PostgreSQL. Also publishes [rls-open-check](https://github.com/LarytheLord/rls-open-check), a Supabase row-level-security linter; its docs report a hand-read sample of 52 findings (27 real, 18 not a problem, 7 unsure).
- **[Open Permit](https://openpermit.vercel.app):** civic tool that drafts evidence-backed objections to factory-farm permit applications. Started at a Code 4 Compassion hackathon.
- **[AFA Resource Chatbot](https://afachatbot.vercel.app):** RAG over the Asia for Animals resource database. Pinecone, OpenAI.
- **Tiger ID hackathon, 25 Oct 2026:** led Team 1. In one day we built an evidence view of 553 facilities from public records and an animal re-identification search. Right tiger first in 98 of 100 cases (1,887 photos, 107 tigers); 52 of 100 for leopards, so only a search aid there.

### Stack

`Python` `C++` `TypeScript` `Go` `SQL` | Numba, NumPy, Array API, CuPy, JAX, PyTorch, Cython, Inspect | Linux, Slurm, Docker, GitHub Actions (including GPU CI), PostgreSQL | Next.js, FastAPI

[llawlietbagsum@gmail.com](mailto:llawlietbagsum@gmail.com) | [abikhn.me](https://abikhn.me) | [Hugging Face](https://huggingface.co/LarytheLord) | [Kaggle](https://www.kaggle.com/larythelord) | [LinkedIn](https://www.linkedin.com/in/abikhn)
