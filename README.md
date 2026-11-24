<!-- ═══════════════════════════  HEADER  ═══════════════════════════ -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Utsav%20Rai&fontSize=64&fontColor=ffffff&fontAlignY=36&desc=backend%20%C2%B7%20LLM%20infra%20%C2%B7%20things%20that%20stay%20up&descAlignY=58&descSize=18&animation=fadeIn" width="100%"/>

<a href="https://github.com/utsxvrai">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=2800&pause=900&color=A78BFA&center=true&vCenter=true&width=720&lines=I+build+backends+that+talk+to+LLMs.;Production+RAG%3A+ingest+%E2%86%92+embed+%E2%86%92+retrieve+%E2%86%92+stream.;Multi-provider+LLM+failover+in+prod.;Payments+%C2%B7+queues+%C2%B7+streaming+%C2%B7+caching.;ICPC+Regionalist+%E2%80%A2+LeetCode+Knight." alt="typing" />
</a>

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-000?style=for-the-badge&logo=vercel&logoColor=white)](https://utsav-rai.vercel.app/)
[![Resume](https://img.shields.io/badge/Resume-111?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1pNnJ8iWeHyPnJWzA0-NylbJyVA-M0iC_/view?usp=sharing)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/utsavrai07)
[![X](https://img.shields.io/badge/@utsxvrai-000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/utsxvrai)

</div>

---

<!-- ═══════════════════════════  WHOAMI  ═══════════════════════════ -->

```ts
// $ cat ~/whoami.ts
const utsav = {
  role:      "Backend Engineer @ Primetrace — consumer AI apps (Tarot99 & Astro99: 10M+ downloads each)",
  base:      "Bengaluru, India",
  ships:     ["production RAG", "multi-provider LLM orchestration", "payments & subscriptions", "event-driven workers"],
  stack:     ["Node.js", "Fastify", "TypeScript", "Python", "FastAPI", "Redis", "MySQL", "AWS"],
  sidequest: "competitive programming — ICPC Regionalist 2025 (AIR 603)",
  motto:     "if it can fail over, it should fail over",
} as const;
```

<!-- ═══════════════════════════  WHAT I'VE SHIPPED  ═══════════════════════════ -->

## ⚡ What I've shipped

<table>
<tr>
<td width="50%" valign="top">

### 🧠 Production RAG platform
Natural-language Q&A over a large community-post corpus.

```
MySQL ─▶ MinHash dedupe ─▶ BGE-M3 ─▶ Qdrant
        streaming GPU ingestion
```
- Re-engineered ingestion to stream on GPU instead of staging huge intermediate files
- FastAPI + Next.js serving: **SSE streaming**, source-cited answers, **MMR reranking**, semantic answer cache
- Idempotent nightly incremental re-index → prototype to live product

</td>
<td width="50%" valign="top">

### 🔀 LLM orchestration layer
AI chat for two apps with **10M+ downloads each**.

```
request ─▶ router ─┬─▶ Gemini
                   ├─▶ Gemma-4-31B   (Bedrock)
                   ├─▶ Qwen3-235B    (Bedrock)
                   └─▶ GPT-5 / Vertex
        provider down? ─▶ automatic failover
```
- Chat, classification & summarisation routed across **AWS Bedrock, Vertex AI, OpenAI**
- Prompt caching + failover keep chat live through upstream outages
- Node.js · Fastify · Sequelize · Redis

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 💳 Payments & subscriptions, end to end
- **Razorpay UPI AutoPay** recurring debits
- **PhonePe** order reconciliation, **Google Play billing**
- Per-country plans
- Async **AWS SQS/SNS** workers for renewals, expiry & attribution

</td>
<td width="50%" valign="top">

### 📞 Voice AI calling — Salesence (intern)
- Backend for an AI outbound-calling platform: **Twilio + ElevenLabs ConvAI**
- Real-time streaming at **~500 ms** with interruption handling
- Lead pipeline with sentiment detection + WhatsApp automation for **100+ concurrent leads** → **90%** faster sales response

</td>
</tr>
</table>

<!-- ═══════════════════════════  OPEN SOURCE  ═══════════════════════════ -->

## 🌍 Open source

Fixing bugs across the Node / TypeScript / LLM-tooling ecosystem — **11 PRs merged** so far.

| | Repo | What |
|---|---|---|
| ✅ merged | [redis/ioredis](https://github.com/redis/ioredis/pull/2300) | malformed RESP no longer leaks into the next command's reply |
| ✅ merged | [OrchestratorInc/agent-orchestrator](https://github.com/OrchestratorInc/agent-orchestrator/pull/8803) | Antigravity Terminal → Chat switch no longer fails on replayed history |
| ✅ merged | [DuarteSantos8/openGym](https://github.com/DuarteSantos8/openGym/pull/1433) | JEFIT import reads real exports with hash-padded headers (ships in 1.4.6) |
| ✅ merged | [genspark-ai/genoffice](https://github.com/genspark-ai/genoffice/pull/2909) | exact point-based line spacing in paragraph formats and styles |
| ✅ merged | [elie222/rakazo](https://github.com/elie222/rakazo/pull/6198) | blank taught-skill names fall back to the goal |
| ✅ merged | [ardia-browser/ardia](https://github.com/ardia-browser/ardia/pull/3320) | toolbar badges round long counts instead of cutting them |
| ✅ merged | [netlify/cli](https://github.com/netlify/cli/pull/11604) | broken CONTRIBUTING link in the PR template |
| ✅ merged | [reticlehq/reticle](https://github.com/reticlehq/reticle/pull/2440) | detached tabs no longer reported as "SDK missing" |
| 👍 approved | [nodejs/undici](https://github.com/nodejs/undici/pull/6242) | unsolicited `100 Continue` no longer kills the socket |
| 👍 approved | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes/pull/8364) | `check` no longer flags text painted by a visible text-shadow |
| 🔍 in review | [PostHog/posthog](https://github.com/PostHog/posthog/pull/140889) | OpenAI long-context generations priced at long-context rates |
| 🔍 in review | [PostHog/posthog-js](https://github.com/PostHog/posthog-js/pull/5860) | n>1 OpenAI chat streams no longer merge their choices |
| 🔍 in review | [prisma/orm](https://github.com/prisma/orm/pull/31160) | dedupe repeated values in `IN` lists |
| 🔍 in review | [meteor/meteor](https://github.com/meteor/meteor/pull/15021) | failed ChangeStream start no longer crashes the server |

<sub>…plus merges in agav, neo-agent-brain, breakinggood and open PRs in sequelize, bitwarden, stdlib, nanocoder, cli-microsoft365 and more — <a href="https://github.com/pulls?q=is%3Apr+author%3Autsxvrai+is%3Apublic+-org%3Akutumbtech">see all</a>.</sub>

<!-- ═══════════════════════════  BUILDS  ═══════════════════════════ -->

## 🛠️ Things I've built

| Project | What it is |
|---|---|
| [**cacheflow**](https://github.com/utsxvrai/Distributed-Cache) · `@cr7bit/cacheflow` | Dual-layer (in-memory + Redis) Node.js cache with auto-failover. Published on npm. |
| [**lfm**](https://github.com/utsxvrai/lfm) | *learn from mistakes* — real backend engineering mistakes, one at a time. |
| [**GrindTech**](https://github.com/utsxvrai/GrindTech) | Prep platform for DSA, system design and backend interviews. |
| AI interview prep platform | Real-time mock interviews: **<500 ms** speech-to-text feedback, 50+ concurrent sessions, **40%** lower AI cost via Redis caching. |

<!-- ═══════════════════════════  STACK  ═══════════════════════════ -->

## 🧰 Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=nodejs,ts,js,python,cpp,fastapi,express,nextjs,react&theme=dark" /><br/>
<img src="https://skillicons.dev/icons?i=redis,mysql,postgres,mongodb,prisma,rabbitmq,aws,docker,githubactions,grafana&theme=dark" />

<br/>

`RAG` · `Qdrant` · `FAISS` · `BGE-M3` · `AWS Bedrock` · `Vertex AI` · `OpenAI` · `SSE` · `WebSockets` · `SQS/SNS` · `event-driven systems`

</div>

<!-- ═══════════════════════════  CP  ═══════════════════════════ -->

## 🏆 Competitive programming

<div align="center">

[![ICPC](https://img.shields.io/badge/ICPC%20Regionalist%202025-Honorable%20Mention%20·%20AIR%20603-1f6feb?style=for-the-badge)](#)
<br/>
[![LeetCode](https://img.shields.io/badge/LeetCode-Knight%20·%201902%20(top%205%25)-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/Kalki21/)
[![Codeforces](https://img.shields.io/badge/Codeforces-Specialist%20·%201433-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/cr7bit)
[![CodeChef](https://img.shields.io/badge/CodeChef-3★%20·%201782-5B4638?style=for-the-badge&logo=codechef&logoColor=white)](https://www.codechef.com/users/cr7bit)

</div>

<!-- ═══════════════════════════  STATS  ═══════════════════════════ -->

## 📈 Activity

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=utsxvrai&show_icons=true&hide_border=true&theme=tokyonight&include_all_commits=true&count_private=true" />
<img height="165" src="https://streak-stats.demolab.com?user=utsxvrai&hide_border=true&theme=tokyonight" />

<img width="95%" src="https://github-readme-activity-graph.vercel.app/graph?username=utsxvrai&theme=tokyo-night&hide_border=true&area=true" />

</div>

<!-- ═══════════════════════════  FOOTER  ═══════════════════════════ -->

<div align="center">

```
> currently: shipping LLM infra in prod, breaking things in staging, fixing them in open source
> open to: interesting backend / AI-infra problems & freelance — DM on X or LinkedIn
```

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=110&section=footer" width="100%"/>

</div>
