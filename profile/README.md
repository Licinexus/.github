<div align="center">

<img src="./logo-white.png" alt="Licinexus" width="320" />

<br/><br/>

# **Vertical AI for Brazilian public procurement**

We build proprietary AI models on top of the **R$ 1,5 trillion/year** that the Brazilian public sector spends. Open data is commodity — the moat is the intelligence we put on top of it.

<br/>

[![Website](https://img.shields.io/badge/licinexus.com.br-050816?style=for-the-badge&logo=googlechrome&logoColor=00d4ff)](https://licinexus.com.br)
[![npm](https://img.shields.io/npm/v/@licinexusbr/mcp?style=for-the-badge&logo=npm&label=%40licinexusbr%2Fmcp&color=cb3837)](https://www.npmjs.com/package/@licinexusbr/mcp)
[![Downloads](https://img.shields.io/npm/dw/@licinexusbr/mcp?style=for-the-badge&logo=npm&label=downloads%2Fweek&color=10b981)](https://www.npmjs.com/package/@licinexusbr/mcp)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/company/licinexus)

</div>

---

## 🎯 The thesis

Brazil runs the largest public procurement market in Latin America. The data is public by law — but lives shattered across **1,000+ federal, state and municipal APIs**, each with its own schema, uptime and breakage. Generic LLMs don't understand CATMAT/CATSER, can't price a winning bid, don't know which clauses raise TCU red flags.

We close that gap with two layers:

1. **Open access to the data** — free and open source, so any supplier, journalist, researcher or public agent can read what's already theirs by law.
2. **A proprietary vertical AI stack** — 7 models trained on 5 years of Brazilian public procurement data, sold to companies that win bids for a living.

> _"We commoditize what any competitor could rebuild in 3 months, to stay focused on what takes 3 years."_

This is *commoditizing your complement* — the playbook Joel Spolsky described, that worked for IBM with Linux and for Google with Android.

---

## 🤖 Our vertical AI stack

Seven proprietary models, purpose-built for Brazilian public procurement. Each one is **continuously retrained as new data arrives daily** from PNCP, Receita Federal, TCU/TCEs and user-feedback loops in the platform — the training set never freezes.

| # | Model | Trained to do | Data foundation (live volumes in our DB) | Status |
|---|---|---|---|---|
| 1 | **Catálogo** | Classify any bid item into the official CATMAT/CATSER taxonomy | 848k curated item → code pairs · 6,49M unified price records · 4,17M historical items · continuously growing | 🟢 **PROD** |
| 2 | **Previsor** | Predict the winning price and the win probability of a bid before the auction opens | 1,49M historical bid outcomes with real winners · daily PNCP refresh · user-feedback on closed bids | 🟢 **PROD** |
| 3 | **OCR** | Extract clean text from edital PDFs and attachments in Brazilian Portuguese | 2,40M edital PDFs in our pipeline (410k already OCRed, growing daily) | 🟢 **PROD** |
| 4 | **Leitor** | Turn any edital PDF into structured data (modality, deadlines, requirements, values, etc) | 2,18M PNCP processes with gold-standard structured fields · 1,01M contracts · 722k atas de registro de preço | 🟡 **BUILD** |
| 5 | **Reader-Full** | Read the full bid document end-to-end and produce a complete viability analysis | Long-context training on full edital documents after OCR · grows with the OCR pipeline | 🟡 **BUILD** |
| 6 | **Auditor** | Detect directional clauses, restrictive requirements and TCU/TCE jurisprudence risk | **10,2M legal documents** across TCU + TCEs (PE, RJ, RO, RS, SC, ES) + Súmulas STF/STJ + CGU + AGU + LexML + DJEN/CNJ + Lei 14.133/2021 + Lei 8.666/1993 + DOU decretos · continuously expanding | 🟡 **BUILD** |
| 7 | **STT** | Transcribe internal calls (SDR, customer meetings, voice notes) in Brazilian Portuguese | Self-hosted speech model tuned for PT-BR business calls · feedback loop from internal usage | 🟡 **BUILD** |

A deep CNPJ graph underpins every model: **65,7M companies + 26,8M shareholders** ingested from Receita Federal, plus **701k curated suppliers** with full bidding history.

**Full family overview** → [licinexus.com.br/ai](https://licinexus.com.br/ai)

---

## 🛠️ Open source

### [`@licinexusbr/mcp`](https://github.com/Licinexus/licinexus-mcp) · first Brazilian MCP server for public procurement

Conecta any LLM (Claude Desktop, Cursor, Cline, ChatGPT) to the National Procurement Portal (PNCP), BrasilAPI, Receita Federal and IBGE — in one command:

```bash
npx -y @licinexusbr/mcp
```

**18 tools · 4 prompts · MIT license · live in the [Official MCP Registry](https://registry.modelcontextprotocol.io).**

[![Stars](https://img.shields.io/github/stars/Licinexus/licinexus-mcp?style=flat-square&logo=github&color=2968ed&label=stars)](https://github.com/Licinexus/licinexus-mcp/stargazers)
[![Forks](https://img.shields.io/github/forks/Licinexus/licinexus-mcp?style=flat-square&logo=github&color=2968ed&label=forks)](https://github.com/Licinexus/licinexus-mcp/network/members)
[![Issues](https://img.shields.io/github/issues/Licinexus/licinexus-mcp?style=flat-square&logo=github&color=10b981&label=open%20issues)](https://github.com/Licinexus/licinexus-mcp/issues)
[![Last commit](https://img.shields.io/github/last-commit/Licinexus/licinexus-mcp?style=flat-square&color=2968ed)](https://github.com/Licinexus/licinexus-mcp/commits/main)

---

## 📊 Premium analyses (proprietary product)

18 AI-powered analyses available in the Licinexus paid product, organized by where they enter your decision flow:

<details open>
<summary><b>🎯 Before bidding</b> — <i>decide IF the bid is worth it</i></summary>

| Analysis | What it does |
|---|---|
| **AI viability** | Whether the bid makes sense for your company — entry cost, achievable margin, requirement fit |
| **AI match + CNAE gate** | Only bids that match your activity and history reach your feed |
| **AI win-chance score** | Score 0-100 per bid, before you spend an hour reading |
| **AI competitor analysis** | Who won historically there, in what price range, with what frequency and win rate |
| **AI institutional intelligence** | Buyer profile, calendar predictability, payment history, institutional risk |
| **AI legal auditor + TCU** | Legal risks, TCU jurisprudence, trap clauses surfaced in seconds |

</details>

<details>
<summary><b>💰 During bidding</b> — <i>decide HOW MUCH to charge</i></summary>

| Analysis | What it does |
|---|---|
| **AI winning-price predictor** | No more guessing the bid — model predicts the price that will win |
| **AI price intelligence** | Fair price across 3 dimensions: temporal (seasonality), regional (your state), institutional (per buyer) |
| **AI margin analysis** | Ceiling price, breakeven price, real margin — before you submit |
| **AI TCU/compliance risk** | Alerts for overpricing, suspect fragmentation, vendor concentration |

</details>

<details>
<summary><b>📄 Documents</b> — <i>stop reading PDFs</i></summary>

| Analysis | What it does |
|---|---|
| **AI edital reader** | 60+ structured fields extracted from any bid PDF |
| **AI CATMAT/CATSER classifier** | Understands each item better than any generic LLM (proprietary model) |
| **AI habilitation checklist** | Extracts all bid requirements and cross-references with your documents |

</details>

<details>
<summary><b>🤝 After winning</b> — <i>protect the contract</i></summary>

| Analysis | What it does |
|---|---|
| **AI contract health** | Time remaining, current vs market value, payment risk — continuous monitoring |
| **AI contract vices** | Detects clauses that historically led to litigation |
| **AI financial intelligence** | Health score per empenho with cash-flow projection |

</details>

<details>
<summary><b>🕵️ Market intelligence & due diligence</b></summary>

| Analysis | What it does |
|---|---|
| **AI supplier prospecting** | Search companies by CNAE, state, size, capital and age — find partners, competitors or B2B leads |
| **AI shareholder network + due diligence** | Maps shareholders, common ownership across CNPJs, inidoneity sanctions and bidding history |

</details>

---

## 📐 By the numbers

<table>
<tr>
<td align="center"><b>R$ 1,5T</b><br/><sub>annual public procurement market</sub></td>
<td align="center"><b>1,000+</b><br/><sub>data sources unified</sub></td>
<td align="center"><b>200k+</b><br/><sub>bids indexed</sub></td>
<td align="center"><b>3,4M</b><br/><sub>items classified</sub></td>
<td align="center"><b>R$ 247B</b><br/><sub>opportunities mapped</sub></td>
</tr>
</table>

---

## 🤝 Work with us

<table>
<tr>
<td width="50%" valign="top">

### 🧑‍💻 Developers
Brazilian-Portuguese govtech is an under-served niche with real production data. We open `good first issue`s weekly in [`licinexus-mcp`](https://github.com/Licinexus/licinexus-mcp/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22). Bilingual (PT/EN), strong CI, DCO sign-off required.

</td>
<td width="50%" valign="top">

### 🏢 Suppliers
Free permanent tier — no credit card. Test the proprietary analyses on real bids at **[licinexus.com.br](https://licinexus.com.br)**.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🔬 Researchers & journalists
The MCP server is the fastest way to cross-reference PNCP with TCU, Receita Federal and IBGE for investigations or academic papers.

</td>
<td width="50%" valign="top">

### 🏛️ Public agencies (B2G)
We are open to partnerships with TCEs, CGUs and procurement bodies for irregularity monitoring and audit automation. → **[licitacao@licinexus.com.br](mailto:licitacao@licinexus.com.br)**

</td>
</tr>
</table>

---

<div align="center">

### **Open source what's commodity. Intelligence where the moat lives.**

[licinexus.com.br](https://licinexus.com.br) · [npm](https://www.npmjs.com/package/@licinexusbr/mcp) · [LinkedIn](https://linkedin.com/company/licinexus) · [licitacao@licinexus.com.br](mailto:licitacao@licinexus.com.br)

<sub>Founded in Juiz de Fora, MG · Brazil 🇧🇷</sub>

</div>
