<p align="center">
  <img src="assets/header.svg" alt="Rajat Kumar Srivastava — Backend engineer. I like finding where the milliseconds go." width="100%" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/rajatsrivastava24/"><img src="https://img.shields.io/badge/LinkedIn-0F1830?style=flat-square&logo=linkedin&logoColor=35D0BA" /></a>
  <a href="mailto:rajatk24srivastava@gmail.com"><img src="https://img.shields.io/badge/Email-0F1830?style=flat-square&logo=gmail&logoColor=FF7A45" /></a>
  <a href="https://srvstvrajat.github.io/Portfolio/"><img src="https://img.shields.io/badge/Portfolio-0F1830?style=flat-square&logo=googlechrome&logoColor=FFB347" /></a>
  <a href="https://codeforces.com/profile/rajat_srvstv"><img src="https://img.shields.io/badge/Codeforces-Expert_1608-0F1830?style=flat-square&logo=codeforces&logoColor=F4D35E" /></a>
  <a href="https://leetcode.com/u/SrvstvRajat"><img src="https://img.shields.io/badge/LeetCode-1809-0F1830?style=flat-square&logo=leetcode&logoColor=FFB347" /></a>
  <img src="https://komarev.com/ghpvc/?username=SrvstvRajat&label=views&color=16213F&style=flat-square" />
</p>

```console
$ whoami
rajat — backend engineer · M.Tech CSE @ IIIT-Delhi (graduating 2027)

$ cat now.txt
studying   graduate systems, algorithms, big data analytics
exploring  tail latency in Kubernetes with eBPF
open to    backend / systems engineering roles and good collabs
```

<br/>

### The trace

Every bar is a span. The three projects sit under the M.Tech span because that is where they happened, and the last two ran side by side.

<p align="center">
  <img src="assets/journey.svg" alt="Timeline from 2019 to 2027: B.Tech at MMMUT, backend SDE at CollegeDunia, M.Tech at IIIT-Delhi, and three projects" width="100%" />
</p>

<br/>

### What moved

<p align="center">
  <img src="assets/impact.svg" alt="Before and after: API latency down 35%, evaluation cost down 96%, p99 up 43% and throughput down 37% under contention" width="100%" />
</p>

<br/>

### Work worth opening

Each one expands into the shape of the system.

<details>
<summary><b>Prepp API performance</b> &nbsp;·&nbsp; CollegeDunia &nbsp;·&nbsp; <code>NestJS</code> <code>GraphQL</code> <code>MongoDB</code> <code>Redis</code></summary>
<br/>

Cut API latency by **35%** by caching hot reads in Redis, tuning MongoDB indexes and restructuring queries across the NestJS/GraphQL services.

</details>

<details>
<summary><b>AI evaluation of handwritten UPSC answers</b> &nbsp;·&nbsp; <code>GPT-4 Vision</code> <code>AWS Textract</code></summary>
<br/>

Cost per evaluation went from about ₹50 to about ₹2 (**96% less**), and the team relies less on human evaluators.

```mermaid
flowchart LR
  A[Handwritten answer] --> B[AWS Textract OCR]
  A --> C[GPT-4 Vision]
  B --> D[Evaluation]
  C --> D
  D --> E[PDF report]
```

</details>

<details>
<summary><b>In-house HLS video pipeline</b> &nbsp;·&nbsp; <code>FFmpeg</code> <code>AWS S3</code></summary>
<br/>

Replaced AWS MediaConvert, removing per-minute conversion charges. Processes 7–8 videos a day.

```mermaid
flowchart LR
  A[Video] --> B[Cron-driven job queue]
  B --> C[FFmpeg HLS<br/>144p to 1080p]
  C --> D[(S3)]
```

</details>

<details>
<summary><b>Payments on Juspay HyperCheckout</b> &nbsp;·&nbsp; <code>REST</code> <code>Webhooks</code></summary>
<br/>

Moved the backend payment workflow to Juspay HyperCheckout. Webhook signatures are validated, and payment events are handled asynchronously so status updates can be trusted.

```mermaid
flowchart LR
  A[Checkout] --> B[Juspay HyperCheckout]
  B -->|webhook| C{Signature valid?}
  C -->|yes| D[Async payment-event handler]
  C -->|no| E[Rejected]
  D --> F[Payment status updated]
```

</details>

<details>
<summary><b>Tail latency in Kubernetes with eBPF</b> &nbsp;·&nbsp; Feb–May 2026 &nbsp;·&nbsp; <code>Kubernetes</code> <code>Docker</code> <code>bpftrace</code></summary>
<br/>

A 3-node cluster running Dockerized microservices, with controlled resource contention applied to benchmark tail latency. Kernel events traced with eBPF/bpftrace pointed to **scheduler-level contention** as the cause of **43% higher p99 latency** and **37% lower throughput**.

```mermaid
flowchart LR
  A[Load] --> B[3-node Kubernetes cluster<br/>Dockerized microservices]
  X[Controlled contention] --> B
  B --> C[eBPF / bpftrace<br/>kernel scheduler events]
  C --> D[p99 +43% · throughput -37%]
```

</details>

<details>
<summary><b>FoodEVPred, async ML inference</b> &nbsp;·&nbsp; Jan–Apr 2026 &nbsp;·&nbsp; <code>Node.js</code> <code>FastAPI</code> <code>Redis</code></summary>
<br/>

Classifies food-derived EV protein sources. A Node.js REST backend fronts a Python/FastAPI inference service; requests are tracked by UUID, batched through Redis, and results are emailed automatically.

```mermaid
flowchart LR
  A[Web UI] --> B[Node.js REST API]
  B -->|UUID request id| C[(Redis)]
  C -->|batch| D[FastAPI inference]
  D --> E[Email result]
```

</details>

<details>
<summary><b>Cellular network capacity simulator</b> &nbsp;·&nbsp; Aug–Dec 2025 &nbsp;·&nbsp; <code>C++</code> <code>Multithreading</code></summary>
<br/>

Object-oriented C++ simulator with users, resource allocation and capacity constraints as separate components. Allocation is multithreaded and keeps shared state consistent under concurrent user operations.

</details>

<br/>

### Toolbox

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,py,cpp,c,go,nodejs,nestjs,express,fastapi,graphql,react&perline=12" /><br/>
  <img src="https://skillicons.dev/icons?i=mongodb,redis,postgres,mysql,kafka,aws,docker,kubernetes,linux,git,github,postman&perline=12" />
</p>

<br/>

### Scoreboard

| | |
|---|---|
| **Codeforces** | Expert, max rating 1608 |
| **LeetCode** | rating 1809, 2000+ problems solved across platforms |
| **GATE CSE 2024** | All India Rank 2543 |
| **Google Hash Code 2021** | rank 414 |
| **Google Kick Start 2021** | global rank 1789 |
| **IIIT-Delhi M.Tech** | CGPA 8.63 · 2025–2027 |
| **MMMUT B.Tech** | CGPA 7.58 · 2019–2023 |

<p align="center">
  <img src="https://leetcard.jacoblin.cool/SrvstvRajat?theme=dark&font=Fira%20Code&ext=heatmap" height="190" alt="LeetCode stats" />
</p>

<br/>

### Contribution graph, eaten

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/SrvstvRajat/SrvstvRajat/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/SrvstvRajat/SrvstvRajat/output/github-snake.svg" />
    <img alt="Contribution snake" src="https://raw.githubusercontent.com/SrvstvRajat/SrvstvRajat/output/github-snake.svg" />
  </picture>
</p>

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=SrvstvRajat&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=SrvstvRajat&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />
</p>

<br/>

<p align="center">
  <i>If you want to talk backend systems, performance, or algorithms, say hi.</i><br/>
  <a href="https://www.linkedin.com/in/rajatsrivastava24/">LinkedIn</a> &nbsp;·&nbsp; <a href="mailto:rajatk24srivastava@gmail.com">Email</a> &nbsp;·&nbsp; <a href="https://www.instagram.com/rajat._srivastava">Instagram</a>
</p>
