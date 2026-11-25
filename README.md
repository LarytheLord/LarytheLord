# Abid Khan

Computer engineering undergraduate, graduating 2028. I work on Numba and GPU performance in scikit-bio, and I test whether LLM judges keep their verdicts when wording changes.

### Google Summer of Code 2026: scikit-bio (NumFOCUS), completed

350-hour project with mentor Dr. Igor Sfiligoi (San Diego Supercomputer Center). I added optional Numba engines next to scikit-bio's Cython code, plus GPU kernels for PERMANOVA, Mantel and PERMDISP and Array API support so the same code runs on NumPy, CuPy, JAX and PyTorch.

- **34 merged PRs**, 20 May to 22 Nov 2026 ([list](https://github.com/scikit-bio/scikit-bio/pulls?q=is:pr+author:LarytheLord+is:merged)).
- **In release 0.7.4 (21 Sep):** Numba engines for PERMANOVA, Mantel, PERMDISP and PCoA, `engine="fast"` for UniFrac, and GPU PERMANOVA and Mantel on NVIDIA and AMD ([release notes](https://github.com/scikit-bio/scikit-bio/releases/tag/0.7.4)). GPU PERMDISP and the condensed-matrix fixes are on main, not yet released.
- **PERMANOVA on one AMD MI300X**, 25,000 samples, 9,999 permutations: 426 s with the Cython code, 30 s with the Numba CPU engine, 7.3 s with the GPU kernel. Mantel: 1,407 s with Cython and 157 s with the GPU kernel (the Numba CPU engine was slower there, 1,547 s). One machine; tables in [#2511](https://github.com/scikit-bio/scikit-bio/pull/2511).
- **PERMDISP** is 10x (centroid test) to 44x (median test) faster than Cython on 5,116-sample Earth Microbiome Project matrices with 128 cores, and still 4x to 6.6x on one thread, so part of that gain comes from removing Python overhead, not from parallelism ([#2547](https://github.com/scikit-bio/scikit-bio/pull/2547)).
- **Bugs I found while testing on real data and hardware:** a float32 accumulation error in PERMANOVA, about 5% off in the F statistic at 25,000 samples ([#2509](https://github.com/scikit-bio/scikit-bio/pull/2509)); GPU-only failures in the Array API paths ([#2530](https://github.com/scikit-bio/scikit-bio/pull/2530)); a PERMDISP seed that never reached PCoA ([#2546](https://github.com/scikit-bio/scikit-bio/pull/2546)).

[![XERJ Corpus Hub contributor](https://hub.xerj.org/contributors/LarytheLord/badge.svg)](https://hub.xerj.org/contributors/LarytheLord)

The PERMDISP GPU kernel was selected for the XERJ Corpus Hub, an open reference that AI coding agents search before writing code.

### LLM evaluation

- **[values-laundering](https://github.com/LarytheLord/values-laundering):** do LLM judges keep a moral verdict when only the wording of an act changes? 81 acts, six rewrite moves, ten judge families from seven labs. My own controls overturned my first headline result, and the repo says so. A ranking found on older models did not hold on 2026 models; the effect of euphemistic rewording on the verdict did. Working paper, not accepted at the NeurIPS 2026 workshops I submitted to; revision in progress. [Dataset](https://huggingface.co/datasets/LarytheLord/values-laundering) (CC-BY-4.0).
- **[same-facts-softer-words](https://github.com/LarytheLord/same-facts-softer-words):** Apart Research sprint, Nov 2026. 11 real incidents from regulator records, six LLM judges. Company statements kept 10 to 40% of the regulator's core facts, and most of the score gap came from the missing facts, not the softer wording. Small study.
- **[inspect-speciesism-eval](https://github.com/LarytheLord/inspect-speciesism-eval):** 106-item evaluation on UK AISI's Inspect framework. Its inspect_evals submission ([#2056](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2056)) was closed unmerged over a corpus-licensing policy; a docs fix there ([#1978](https://github.com/UKGovernmentBEIS/inspect_evals/pull/1978)) was merged.
- **Global Open-source AI Challenge 2026, Hangzhou:** one of 20 semifinalists in the AI for Research track. Defended it live to a panel in Sept 2026; did not reach the final.

### Open source

**69 merged PRs in 27 projects run by other people**, 34 of them in scikit-bio. Of the other 35, 22 are docs fixes and 12 change 10 lines or fewer (the two groups overlap). The code fixes I would point to: a hung stdin in [Daytona](https://github.com/daytonaio/daytona/pull/4107), a resource leak in [Docling](https://github.com/docling-project/docling/pull/3134), `llm_base_url=""` handling in [OpenHands](https://github.com/All-Hands-AI/OpenHands/pull/13471), quieter auth failures in [codecarbon](https://github.com/mlco2/codecarbon/pull/1080). Smaller merged PRs are in Helm, Kubernetes, Nextflow, scanpy, pyinaturalist and pygbif. [Search: everything I have merged outside my own repos](https://github.com/search?q=author%3ALarytheLord+is%3Apr+is%3Amerged+-user%3ALarytheLord&type=pullrequests) (86 results: it also includes 17 PRs in hackathon and team repos).

### Other projects

- **[Adventurers Guild](https://www.guilds.work):** marketplace for scoped developer tasks, with a multi-agent QA review step. Next.js, Prisma, PostgreSQL.
- **[rls-open-check](https://github.com/LarytheLord/rls-open-check):** linter for Supabase row-level-security mistakes. I read 52 of its findings by hand: 27 real, 18 not a problem, 7 unsure, and published that.
- **[Open Permit](https://openpermit.vercel.app):** drafts evidence-backed objections to factory-farm permit applications. Started at a Code 4 Compassion hackathon.
- **[AFA Resource Chatbot](https://afachatbot.vercel.app):** retrieval-augmented chatbot over the Asia for Animals resource database (Pinecone, OpenAI).
- **Tiger ID hackathon, 25 Oct 2026:** led Team 1. In one day we built an evidence view of 553 facilities from public records and a tiger re-identification search: right tiger first in 98 of 100 cases (1,887 photos, 107 tigers), 52 of 100 for leopards, so only a search aid there.

### Stack

Python, C++, TypeScript, Go, SQL. Numba, NumPy, Cython, CuPy, JAX, PyTorch, Inspect. Linux, Slurm, Docker, GitHub Actions (including GPU CI), PostgreSQL. Next.js, FastAPI.

[llawlietbagsum@gmail.com](mailto:llawlietbagsum@gmail.com) | [abikhn.me](https://abikhn.me) | [Hugging Face](https://huggingface.co/LarytheLord) | [Kaggle](https://www.kaggle.com/larythelord) | [LinkedIn](https://www.linkedin.com/in/abikhn)
