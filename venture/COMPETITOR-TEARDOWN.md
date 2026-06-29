# Crédito Distun — Competitor Teardown & Feature Differentiation

Real-product-team teardown of the closest analogs' actual product/UX, the feature differentiation matrix, the defensible wedge, and the MVP scope. Cited where possible; `[needs verification]` where not.

## Product teardowns (what they actually do)

- **Slope** (US embedded capital) — instant cash-flow underwriting ("SlopeScore"), embedded at digital checkout via API, net-30/60 + installments, J.P. Morgan debt facility behind it. *Nails:* genuine embedded capital on a real balance sheet. *Gap:* US-only; assumes digital checkout + ACH/card + US bank/bureau data — none of which a thin-file Guatemalan ferretería at a counter has.
- **R2** (LatAm, Capital-as-a-Service) — underwrites the SMB off the *platform's* proprietary data (Rappi/Clip sales), repaid by skimming a % of daily sales. *Nails:* turns platform data into self-amortizing credit. *Gap:* needs a digital platform capturing the merchant's **sales** flow; a distributor sees what a store **buys**, not sells. Every partner is consumer-facing digital.
- **Kontempo** (Mexico) — "Credit CRM for the industrial sector"; distributor-initiated credit via WhatsApp payment link, no card/bank required, AI collections. *Nails:* localized to how MX industrial trade credit runs. *Gap:* drifting up-market (CEMEX/Walmart, $100K–$10M lines), not the neighborhood ferretería; risk-ownership undisclosed `[needs verification]`.
- **Tul / CrediTUL** (CO/MX/BR) — *closest analog*: revolving line embedded in a hardware-ordering app, 30/45/60-day terms, purpose-bound to inventory bought **from Tul**. *Nails:* credit embedded in the distribution flow. *Gap:* a **closed competing marketplace** (finances inventory bought from Tul), not credit infra another distributor can plug into; underwriting inputs undisclosed; disintermediates the distributor.
- **Addi** (CO) — best-in-class **consumer** BNPL; cédula + WhatsApp → bureau pull + ML → offer in seconds. *Nails:* near-zero-friction instant decisioning UX. *Gap:* underwrites individuals off a **bureau**; wrong borrower, wrong (fixed-installment) shape, sits at a retailer's consumer checkout.
- **Mercado Crédito** (the unsecured-SME benchmark) — proprietary-data ML, pre-approved/invitation-only, collected off MP sales flow. *Nails:* closed-loop flywheel. *Gap:* requires the borrower's **own sales** through MP; no cold-start, no distributor-embedded origination.

## Feature differentiation matrix

| Capability | Slope | R2 | Kontempo | Tul | Addi | **Crédito Distun** |
|---|:--:|:--:|:--:|:--:|:--:|:--:|
| Underwritten on **proprietary purchase history** | partial | partial | ✗ | partial | ✗ | **✓** |
| **Embedded in distributor order flow** | ✗ | ✗ | partial | ✓ | ✗ | **✓** |
| **Sales-rep-tablet origination** | ✗ | ✗ | partial | partial | ✗ | **✓** |
| **Pay-when-job-pays / job-based terms** | ✗ | partial | ✗ | ✗ | ✗ | **✓** |
| **No-bureau thin-file approval** | partial | ✓ | partial | partial | ✗ | **✓** |
| Originate-and-sell / factoring | partial | ✓ | partial | ✗ | ✗ | partial (roadmap) |
| **Merchant-funded free tier** (net-30) | ✗ | ✗ | partial | partial | ✓ | **✓** |
| Multi-distributor platform | ✓ | ✓ | ✓ | ✗ | ✓ | ✗ (v2+) |
| Spanish-first LatAm | ✗ | ✓ | ✓ | ✓ | ✓ | **✓** |

## The differentiated wedge (why competitors structurally can't copy)
1. **Underwritten on AG's buy-side purchase history.** Everyone else underwrites the borrower's *sales*, a *bureau*, or *bank feeds* — all absent for thin-file ferreterías. AG sees years of what a store buys + whether it pays the distributor. You can't replicate AG's ledger without being AG's distribution arm.
2. **Origination at the point of order** on the rep tablet / counter — the highest-intent moment, owned by the trusted rep. Others reach into a digital checkout that doesn't exist here.
3. **Job-based "pay when the job pays" terms** — net-60/90 sized to the contractor's estimación cycle, only credible when you can see purchase cadence.
4. **Merchant-funded free net-30** — AG captures upstream order margin, so a 2% MDR-funded free tier is rational for AG and undercuts every pure-play lender.

## MVP feature set vs later
**v1 (must-have / the demo):** rep-tablet + counter origination; rules-based purchase-history underwriting → instant pre-approved limit; transparent terms selector (net-30 free / net-60-90 fee); thin-file KYC + e-sign; repayment + reconciliation; WhatsApp reminders; distributor ops dashboard.
**v2+:** wallet + card; originate-and-sell/factoring rail; multi-distributor platform (the network); ML underwriting (as the loss curve matures); true job-linked repayment triggers; buyer self-serve app.

*Sequencing: v1 proves the wedge only AG can build (proprietary-data underwriting embedded at point-of-order) on one distributor where data + incentives align. Everything else is scale/monetization that pays off only after the loss curve is proven.*
