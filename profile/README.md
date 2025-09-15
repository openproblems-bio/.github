# Open Problems in Single‑Cell Analysis

**Define and benchmark challenges in single-cell data science via open standards and continuous leaderboards to promote method development and guide users in method selection.**
This organization hosts the code, tasks, datasets, and docs behind the Open Problems platform.

* **Website & docs:** [openproblems.bio](https://openproblems.bio) · [Documentation](https://openproblems.bio/documentation)
* **Leaderboards:** [Benchmarks](https://openproblems.bio/benchmarks)
* **Datasets browser:** [Datasets](https://openproblems.bio/datasets)
* **Community:** [Discord](https://discord.com/invite/PEmRN4tjvE) · [Interest form](https://docs.google.com/forms/d/e/1FAIpQLSe90Oky4-1b0HbdLsp5Yqo9juCd2mq-NlGHU9NHRW1ECok1xQ/viewform?usp=sf_link)

---

## What lives in this org

* **Core platform** - [`openproblems`](https://github.com/openproblems-bio/openproblems): the living, extensible, community‑guided benchmarking framework.
* **Common datasets** - [`datasets`](https://github.com/openproblems-bio/datasets): workflows for managing and processing common datasets.
* **Benchmarks as repositories**: task‑specific repos named `task_*` (e.g., `task_batch_integration`, `task_label_projection`, `task_spatially_variable_genes`, etc.).
* **Task template** - [`task_template`](https://github.com/openproblems-bio/task_template): scaffolding to start a new benchmark with the correct structure.
* **Shared libraries & images** - [`core`](https://github.com/openproblems-bio/core): helper R/Python packages and base Docker images used across tasks.

---

## How the platform works (in short)

More detailed documentation below.

* **Tasks** define an API, reference datasets, and **quantitative metrics**.
* **Methods** implement that task API.
* **Continuous evaluation** runs standardized workflows to score methods and update leaderboards.
* **Reproducibility** is enforced via containers and declarative workflows.

**Tech stack highlights:**

* **Nextflow** for portable workflows; **Viash** for modular components; **AnnData** for standardized I/O; **GitHub Actions** for CI; deployment via **Nextflow Tower** with cloud backends (e.g., AWS Batch/S3). See the [Technology stack](https://openproblems.bio/documentation/advanced_topics/technology_stack) for details.

---

## Quick start

1. **Explore current leaderboards**
   Check out live tasks and results on the [Benchmarks](https://openproblems.bio/benchmarks) page.

2. **Run a benchmark locally**
   Read the platform [Documentation](https://openproblems.bio/documentation) for install requirements and common commands. Components are containerized; workflows run on laptop, HPC, or cloud.

3. **Add your method to a task**
   Follow the docs ("Create component → Add a method") and open a PR in the corresponding `task_*` repo. See repo READMEs for task‑specific APIs.

4. **Propose or start a new task**
   Start from [`task_template`](https://github.com/openproblems-bio/task_template) and the docs ("Create a new task"). Open an issue to coordinate scope and maintainership.

5. **Join the community**

   * Chat: [Discord](https://discord.com/invite/PEmRN4tjvE)
   * Working meetings: [Join our weekly working meetings](https://openproblems.bio/events/weekly_coworking)
   * Announcements & events: [Interest form / mailing list](https://docs.google.com/forms/d/e/1FAIpQLSe90Oky4-1b0HbdLsp5Yqo9juCd2mq-NlGHU9NHRW1ECok1xQ/viewform?usp=sf_link)
   * Events archive: [openproblems.bio/events](https://openproblems.bio/events)

---

## Governance & community expectations

* **Governance:** Open, consensus‑seeking model with defined roles (Core team, Task teams, Infrastructure, etc.). Read the current [Governance](https://openproblems.bio/documentation/more_information/governance).
* **Code of Conduct:** We follow the Contributor Covenant. Report issues to **[community@openproblems.bio](mailto:community@openproblems.bio)**. See the full [Code of Conduct](https://openproblems.bio/documentation/more_information/code-of-conduct).

---

## Citation

If you use Open Problems, please cite:

> Luecken, M.D., Gigante, S., Burkhardt, D.B. *et al.* **Defining and benchmarking open problems in single‑cell analysis.** *Nature Biotechnology* (2025).
> [https://doi.org/10.1038/s41587-025-02694-w](https://doi.org/10.1038/s41587-025-02694-w)

To reference specific tasks or datasets, please cite the corresponding task or dataset publications mentioned in the task descriptions and dataset pages. For example, to reference our Open Problems multimodal BMMC datasets, please cite Luecken et al., NeurIPS 2021.

Also see earlier NeurIPS challenge reports and proceedings referenced on the [Events](https://openproblems.bio/events) page.

---

## Licensing

Open Problems is free open source software and distributed under the [MIT License](https://opensource.org/license/mit). However, Open Problems tasks may include references to data or code distributed by a third party under a different license. If any question about license arises, please consult the specific repository in which a particular asset is hosted. If further clarification is needed, please open a GitHub Issue referencing the asset if any clarification is needed.

* **Code** in this org is **MIT** unless stated otherwise in the repo.
* The **website** repo uses mixed licensing: Markdown/JSON content under **CC‑BY‑4.0** and code under **MIT** (see that repo's LICENSE files).
* **Datasets** retain their **original source licenses/terms**; check dataset pages before downstream use.

---

## Acknowledgments

Open Problems is supported by a growing community and sponsors including the [**Chan Zuckerberg Initiative**](https://chanzuckerberg.com/), [**Data Intuitive**](https://www.data-intuitive.com/), [**Helmholtz Munich**](https://www.helmholtz-munich.de/en), [**Saturn Cloud**](https://saturncloud.io/), and [**Seqera**](https://seqera.io/). See the website for the latest list.

---

## Development notes

* Primary languages: **Python** and **R** (task repos may include Bash/Nextflow/TeX for workflows and docs).
* CI builds and unit tests run via **GitHub Actions**; component images are maintained centrally in `core`.

---

### Maintainers & contact

* Issues and PRs: use the relevant repo (`openproblems` or `task_*`).
* Community and governance questions: **[community@openproblems.bio](mailto:community@openproblems.bio)**.
* Real‑time chat: [Discord](https://discord.com/invite/PEmRN4tjvE).
