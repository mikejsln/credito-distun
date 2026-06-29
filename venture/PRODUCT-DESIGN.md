# Crédito Distun — Product Design (Personas · Journey · UI Flow · Walkthrough)

The discovery→design spine behind the interactive demo (`/app/`). Built the way a real product team would: who it's for, the end-to-end journey, the screen flow + states, and the narrated walkthrough.

## Personas
- **Doña Marta Xitumul — ferretería owner/buyer (PRIMARY).** Owns Ferretería La Bendición, Chimaltenango; 6-yr Distun account (~Q45k/mo). No bank credit; runs on cash + informal 8-day terms. *Goal:* say "yes" to a Q60k order on terms in 90 seconds without a bank. *Quote:* "Distun sí sabe quién soy — me conocen hace seis años."
- **Ing. Byron Cux — small/mid contractor.** Q150k–Q800k jobs; squeezed by the gap between buying materials now and getting paid on the estimación 30–60 days later. *Goal:* terms that line up with when the obra pays.
- **Kevin Tzep — Distun sales rep (TABLET OPERATOR).** Visits ~14 ferreterías/day. *Goal:* close bigger orders without personally carrying the "¿le fío o no?" credit risk. *Quote:* "Yo sé quién paga. Si la tablet lo decide, yo solo vendo."
- **Lic. Andrea Robles — credit-ops lead (PORTFOLIO).** Owns underwriting policy + portfolio health. *Goal:* grow volume while loss stays under target; trace every approval to its purchase-history signals.

## Journey map — Doña Marta financing an order
| Stage | Action | Feel | Pain today | Crédito Distun opportunity |
|---|---|---|---|---|
| Need/Trigger | Byron asks for Q60k materials, pays her in ~45 days | anxious | can't float inventory | pre-qualified line surfaced *before* the order |
| Order build | Marta + Kevin assemble the cart | doing cash math | starts cutting quantities | credit shown as a first-class pay option in-cart |
| Financing decision | picks net-30 vs net-60/90 | skeptical ("the catch?") | only informal/10%-mo lenders | transparent terms, fee in Quetzales upfront |
| Approval | taps Solicitar | tense → relieved/proud | bank = weeks, fiador, "no" | instant decision on 6-yr history; *shows the why* |
| Fulfillment | order ships from depot | confident | stockouts | ships on credit, no cash out |
| Job / get paid | crew uses material; municipality pays Byron | calm | cash trapped in stock | working capital freed |
| Repay | repays via rep / link / transfer | wants painless | notebook tracking | one-tap, reminders; on-time grows the limit |
| Re-order | line refreshes & grows | empowered | each cycle from zero | revolving line → flywheel (more buying → more data → higher limit) |

*Emotional arc: anxiety → skepticism → relief/pride → empowerment.*

## UI flow / information architecture (rep-tablet POV)
`Ruta del día → Cliente (Resumen+línea) → Nuevo pedido → Forma de pago → Plazo → Decisión de crédito → Confirmación → Pagos`; plus the **Cartera (ops)** dashboard.

Happy path + the states that make it real:
1. **Ruta del día** — visit list; each stop badged `Crédito: Q__` / `Evaluar` / `En mora`. States: empty/loading/default/alert.
2. **Perfil del cliente** — line card, utilization, KPIs (avg buy, on-time ratio, tenure), 12-mo purchase sparkline. States: active line / no line / suspended.
3. **Nuevo pedido** — SKU cart, bulk-discount nudge, over-limit inline warning. States: empty / items / over-limit.
4. **Forma de pago** — Contado vs Crédito Distun (badge: available). States: available / not-available / partial.
5. **Plazo** — net-30 free / net-60 / net-90 with fee + due date + total, recomputed live.
6. **Decisión de crédito (THE MOAT SCREEN)** — "Analizando historial Distun…" → verdict + **"Por qué aprobamos" signal panel** (tenure, volume+trend, payment consistency, recency, product mix) + composite score + data lineage. States: **loading / approved / partial-limit (counter-offer + split) / declined (with the limiting signal + path back) / cold-start (welcome line + growth path)**.
7. **Confirmación → Pedido confirmado** — OTP sign, line updates, due-date reminder.
8. **Pagos** — outstanding, due date, record/parcial/SMS link; on-time toast ("tu límite puede subir").
★ **Cartera (ops)** — originated/yr, utilization, loss/cycle, approval rate, DPD buckets, loss by zone; every approval traceable to its signals.

## Demo walkthrough (the guided tour, 8 steps)
1. **Meet the customer** — the Q75k line exists *because of* the relationship (pre-computed, not applied for).
2. **A real order** — Q60k municipal-job order; lives at the point of order inside the rep's motion.
3. **Credit as a pay option** — embedded finance, where the buy decision happens.
4. **Terms in plain Quetzales** — transparent, merchant-funded-free; no hidden interest.
5. **The moat: the decision and its WHY** — 6 signals → Score 82; AG underwrites thin-file no bank touches, explainably. *(the hero moment)*
6. **The honest branch** — partial-limit counter-offer with a clean split; degrades gracefully, never loses the sale.
7. **Close the loop, start the flywheel** — OTP confirm, line updates, repayment begins; the line grows.
8. **The portfolio view** — a real lending business with governable risk, not a checkout feature.

**So what:** proprietary underwriting moat + solved distribution (≈$0 CAC) + aligned/expandable economics + a large underserved TAM = a fundable credit *platform*, not a feature.
