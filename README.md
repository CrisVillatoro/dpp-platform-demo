# AI-Powered Digital Product Passport Platform Demo

**Sopra Steria · Industrial & Manufacturing Practice**

A consulting-grade, browser-based demonstration of an AI-powered Digital Product Passport (DPP) platform for the battery and OEM sector, built ahead of the EU Battery Regulation deadline of **18 February 2027**.

---

## What is a Digital Product Passport?

A Digital Product Passport (DPP) is a structured digital record that captures the full lifecycle of a product — materials, carbon footprint, supply chain, performance, and end-of-life data. Under **EU Regulation 2023/1542** (Battery Regulation) and the broader **ESPR framework (EU 2024/1781)**, a Battery Passport becomes mandatory for industrial and EV batteries from February 2027.

---

## What this demo shows

This demo simulates a production DPP platform built on top of a Data Hub, featuring:

- **Portfolio view** — compliance readiness scores across a battery product fleet
- **Product Detail (DPP view)** — all 7 regulatory categories with AI-generated regulatory insights per attribute
- **Compliance Cockpit** — gap analysis, attribute register, audit package generation, and gap register export
- **Regulatory Radar** — EU timeline from 2023 to 2030 with ESPR delegated acts
- **Agent Dashboard** — four AI agents automating compliance tasks (regulatory monitoring, data completeness, attribute lifecycle, audit preparation)
- **Interoperability** — Eclipse BaSyx / Asset Administration Shell (AAS) integration and multi-format export
- **DPP Merge Wizard** — combine N battery products into a single compliant merged passport
- **DPP Guide** — explainer page with QR code section and self-assessment checklist
- **AI Assistant** — in-app chatbot with regulatory Q&A

---

## How to run

1. Clone this repository
2. Open `dpp-demo.html` in any modern browser (Chrome, Edge, Firefox, Safari)
3. The logo file `SOPRASTERIA_logo_RVB_blanc_exe.png` must be in the **same folder** as the HTML file

No internet connection, server, or installation required. The demo is fully self-contained.

```bash
git clone https://github.com/CrisVillatoro/dpp-platform-demo.git
cd dpp-platform-demo
open dpp-demo.html   # macOS
# or double-click dpp-demo.html in Finder / Explorer
```

---

## Repository contents

| File | Description |
|---|---|
| `dpp-demo.html` | The full interactive demo — single self-contained HTML file |
| `SOPRASTERIA_logo_RVB_blanc_exe.png` | Sopra Steria logo — must stay alongside the HTML |
| `DPP-Demo-UserGuide.md` | Presenter guide with demo narrative and walkthrough |

---

## Regulatory coverage

The demo data structure mirrors the mandatory attributes under:

- **EU 2023/1542** — Battery Regulation (Annex XIII)
- **EU 2024/1781** — Ecodesign for Sustainable Products Regulation (ESPR)

Seven regulatory categories are covered: Battery Carbon Footprint, Materials & Composition, Circularity & Resource Efficiency, Identifiers & Traceability, Performance & Durability, Supply Chain Due Diligence, and Conformity & Labelling.

---

## Architecture (production reference)

```
Data Hub (system of record)
      │
DPP API Gateway (transformation & validation layer)
      │
BaSyx AAS Registry (IDTA standard — system of exchange)
      │
EU DPP Registry / Market Surveillance Authorities
```

AI agents in the demo represent Claude API-powered services for regulatory monitoring, data completeness enforcement, attribute lifecycle management, and audit preparation. All agents operate on a **human-in-the-loop** governance model — they propose, never auto-publish.

---

## Customising for a client

Before presenting, update these elements in `dpp-demo.html` (clearly labelled in the JavaScript section):

- Product names and readiness scores (`PRODUCTS` object)
- Persona labels (`PERSONAS` object)
- Chatbot pre-scripted responses (`RESPONSES` object)
- Days-to-deadline counter (search for `daysLeft`)

---

*Internal use — Sopra Steria. C2 — Usage restreint.*
