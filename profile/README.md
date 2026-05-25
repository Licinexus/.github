<div align="center">

<img src="./logo-white.png" alt="Licinexus" width="320" />

<br/><br/>

# **Vertical AI for Brazilian public procurement**

We build proprietary AI models on top of the trillion-real Brazilian public sector procurement market. Open data is commodity, the moat is the intelligence we put on top of it.

<br/>

[![Website](https://img.shields.io/badge/licinexus.com.br-050816?style=for-the-badge&logo=googlechrome&logoColor=00d4ff)](https://licinexus.com.br)
[![npm](https://img.shields.io/npm/v/@licinexusbr/mcp?style=for-the-badge&logo=npm&label=%40licinexusbr%2Fmcp&color=cb3837)](https://www.npmjs.com/package/@licinexusbr/mcp)
[![Downloads](https://img.shields.io/npm/dw/@licinexusbr/mcp?style=for-the-badge&logo=npm&label=downloads%2Fweek&color=10b981)](https://www.npmjs.com/package/@licinexusbr/mcp)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/company/licinexus)

</div>

---

## The thesis

Brazil runs the largest public procurement market in Latin America. The data is public by law, but lives shattered across federal, state and municipal portals, each with its own schema, uptime and breakage. Generic LLMs don't understand CATMAT/CATSER, can't price a winning bid, don't know which clauses raise TCU red flags.

We close that gap with two layers:

1. **Open access to the data**, free and open source, so any supplier, journalist, researcher or public agent can read what's already theirs by law.
2. **A proprietary vertical AI stack**, models fine-tuned on Brazilian public procurement data, sold to companies that win bids for a living.

> *"We commoditize what any competitor could rebuild quickly, to stay focused on what takes years."*

This is *commoditizing your complement*, the playbook Joel Spolsky described that worked for IBM with Linux and for Google with Android.

---

## Our vertical AI stack

Proprietary models purpose-built for Brazilian public procurement. Each one is **continuously retrained as new data arrives daily** from public Brazilian sources and user-feedback loops in the platform. The training set never freezes.

| # | Model | Trained to do | Status |
|---|---|---|---|
| 1 | **Catálogo** | Classify any bid item into the official CATMAT/CATSER taxonomy | PROD |
| 2 | **Previsor** | Predict the winning price and the win probability of a bid before the auction opens | PROD |
| 3 | **CNAE Matcher** | Semantic match between bid descriptions and supplier CNAE codes | PROD |
| 4 | **Leitor** | Turn any edital PDF into structured data (modality, deadlines, requirements, values, etc) | PROD |
| 5 | **OCR** | Extract clean text from edital PDFs and attachments in Brazilian Portuguese | PROD |
| 6 | **Reader-Full** | Read the full bid document end-to-end and produce a complete viability analysis | BUILD |
| 7 | **Auditor** | Detect directional clauses, restrictive requirements and jurisprudence risk | BUILD |
| 8 | **STT** | Transcribe internal calls in Brazilian Portuguese | BUILD |

A CNPJ graph underpins every model, ingested from Receita Federal public data, plus curated supplier history.

**Full family overview** → [licinexus.com.br/ai](https://licinexus.com.br/ai)

---

## Open source

### [`@licinexusbr/mcp`](https://github.com/Licinexus/licinexus-mcp) · first Brazilian MCP server for public procurement

Connect any LLM client (Claude Desktop, Cursor, Cline, ChatGPT) to the National Procurement Portal (PNCP), BrasilAPI, Receita Federal and IBGE in one command:

```bash
npx -y @licinexusbr/mcp
```

**18 tools · 4 prompts · MIT license · live in the [Official MCP Registry](https://registry.modelcontextprotocol.io).**

[![Stars](https://img.shields.io/github/stars/Licinexus/licinexus-mcp?style=flat-square&logo=github&color=2968ed&label=stars)](https://github.com/Licinexus/licinexus-mcp/stargazers)
[![Forks](https://img.shields.io/github/forks/Licinexus/licinexus-mcp?style=flat-square&logo=github&color=2968ed&label=forks)](https://github.com/Licinexus/licinexus-mcp/network/members)
[![Last commit](https://img.shields.io/github/last-commit/Licinexus/licinexus-mcp?style=flat-square&color=2968ed)](https://github.com/Licinexus/licinexus-mcp/commits/main)

---

## Premium analyses (proprietary product)

AI-powered analyses available in the Licinexus paid product, organized by where they enter your decision flow:

<details open>
<summary><b>Before bidding</b>, <i>decide IF the bid is worth it</i></summary>

| Analysis | What it does |
|---|---|
| **AI viability** | Whether the bid makes sense for your company, entry cost, achievable margin, requirement fit |
| **AI match + CNAE gate** | Only bids that match your activity and history reach your feed |
| **AI win-chance score** | Score per bid, before you spend an hour reading |
| **AI competitor analysis** | Who won historically there, in what price range, with what frequency and win rate |
| **AI institutional intelligence** | Buyer profile, calendar predictability, payment history, institutional risk |
| **AI legal auditor + jurisprudence** | Legal risks, jurisprudence references, trap clauses surfaced in seconds |

</details>

<details>
<summary><b>During bidding</b>, <i>decide HOW MUCH to charge</i></summary>

| Analysis | What it does |
|---|---|
| **AI winning-price predictor** | Predicts the price likely to win |
| **AI price intelligence** | Fair price across 3 dimensions: temporal, regional, institutional |
| **AI margin analysis** | Ceiling price, breakeven, real margin before you submit |
| **AI compliance risk** | Alerts for overpricing, suspect fragmentation, vendor concentration |

</details>

<details>
<summary><b>Documents</b>, <i>stop reading PDFs</i></summary>

| Analysis | What it does |
|---|---|
| **AI edital reader** | Structured fields extracted from any bid PDF |
| **AI CATMAT/CATSER classifier** | Understands each item with the vertical context built in |
| **AI habilitation checklist** | Extracts all bid requirements and cross-references with your documents |

</details>

<details>
<summary><b>After winning</b>, <i>protect the contract</i></summary>

| Analysis | What it does |
|---|---|
| **AI contract health** | Time remaining, current vs market value, payment risk, continuous monitoring |
| **AI contract vices** | Detects clauses that historically led to litigation |
| **AI financial intelligence** | Health score per empenho with cash-flow projection |

</details>

<details>
<summary><b>Market intelligence and due diligence</b></summary>

| Analysis | What it does |
|---|---|
| **AI supplier prospecting** | Search companies by CNAE, state, size, capital and age |
| **AI shareholder network and due diligence** | Maps shareholders, common ownership across CNPJs, sanctions and bidding history |

</details>

---

## Work with us

<table>
<tr>
<td width="50%" valign="top">

### Developers
Brazilian-Portuguese govtech is an under-served niche with real production data. We open `good first issue` items weekly in [`licinexus-mcp`](https://github.com/Licinexus/licinexus-mcp/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22). Bilingual (PT/EN), strong CI, DCO sign-off required.

</td>
<td width="50%" valign="top">

### Suppliers
Free permanent tier, no credit card. Test the proprietary analyses on real bids at **[licinexus.com.br](https://licinexus.com.br)**.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Researchers and journalists
The MCP server is the fastest way to cross-reference PNCP with public registries for investigations or academic papers.

</td>
<td width="50%" valign="top">

### Public agencies (B2G)
We are open to partnerships with control bodies and procurement agencies for irregularity monitoring and audit automation, **[licitacao@licinexus.com.br](mailto:licitacao@licinexus.com.br)**.

</td>
</tr>
</table>

---

<div align="center">

### **Open source what's commodity. Intelligence where the moat lives.**

[licinexus.com.br](https://licinexus.com.br) · [npm](https://www.npmjs.com/package/@licinexusbr/mcp) · [LinkedIn](https://linkedin.com/company/licinexus) · [licitacao@licinexus.com.br](mailto:licitacao@licinexus.com.br)

<sub>Founded in Juiz de Fora, MG, Brazil</sub>

</div>
