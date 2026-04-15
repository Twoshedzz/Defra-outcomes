# Defra Outcomes Framework — reference extract

This file is a **verbatim-style reference** of content supplied for the outcomes framework (including outcome owners). Use it alongside `defra-outcomes-framework.md` and `app/data/outcomes.json` — **`outcomes.json` drives the HTML prototype.**

**Visual hierarchy (Defra infographic):** a reference screenshot is stored in the repo as [`reference/defra-outcomes-framework-infographic.png`](reference/defra-outcomes-framework-infographic.png) (vision, four coloured pillars, resilience row).

---

## Defra vision

**Restoring nature, supporting growth, enhancing security**

As the steward of our natural resources, we strengthen the foundations of our economy and our national security.

---

## Secretary of State priorities → Outcomes

### 1. Restoring nature while supporting development

- **Housing and infrastructure that is environmentally positive**  
  **Outcome owner:** Toby Nation, Director Environmental Quality, Infrastructure and Planning.

- **Thriving habitats and wildlife**  
  **Outcome owner:** Deb Hankins, Director Biodiversity, Land Use and Investment.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Thriving, productive seas**  
  **Outcome owner:** Gareth Baynham-Hughes, Director Marine and Fisheries.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Nature accessible and enjoyable for all**  
  **Outcome owner:** Edward Barker, Director Strategy, Governance and Climate.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

---

### 2. Reforming our water system so it drives growth, protects consumers and enhances the environment

- **Resilient, reliable and safe supply of water to homes and businesses**  
  **Outcome owner:** David Hallam, Director Floods and Water.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Clean rivers, lakes and seas**  
  **Outcome owner:** David Hallam, Director Floods and Water.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

---

### 3. Backing British farming and food industry to boost production

- **Profitable, productive, sustainable farming sector**  
  **Outcome owner:** Mike Rowe, Director Farming and Countryside.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Profitable and resilient food sector that provides affordable, nutritious food**  
  **Outcome owners:** Charlotte Baker & Tessa Jones, Directors Agri-Food Chain.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

---

### 4. Resetting trading relationships, including with the EU

- **Trade barriers with the EU reduced for food, plants and animals**  
  **Outcome owner:** Mark Thompson, Director Trade Delivery and EU Reset Government Legislation.

- **Increased trade that supports domestic production, high food standards and downward pressure on food prices**  
  **Outcome owner:** Sophie Brice, Director EU and International Trade.

---

## Resilience and Security outcomes

- **Lower greenhouse gas emissions**  
  **Outcome owner:** Edward Barker, Director Strategy, Governance and Climate.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Climate adaptation**  
  **Outcome owner:** Edward Barker, Director Strategy, Governance and Climate.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Protection from pollution and environmental hazards**  
  **Outcome owner:** Toby Nation, Director Environmental Quality, Infrastructure and Planning.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Minimise waste, tackle waste crime, maximise use of resources**  
  **Outcome owner:** Simon James, Director Circular Economy.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.  
  *(Source text used the label “Outcomes owner” — treated as “Outcome owner” in structured data.)*

- **Resilience to flooding**  
  **Outcome owner:** Sebastian Catovsky, Director Floods and Water.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Emergency preparedness and response to environmental incidents, disease outbreaks, food and water supply shocks**  
  **Outcome owner:** Rebecca Shrubsole, Director Ministerial, Growth and Resilience.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Robust biosecurity**  
  **Outcome owner:** Anjali Juneja, Director Animal and Plant Health and Welfare.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Good animal welfare**  
  **Outcome owner:** Anjali Juneja, Director Animal and Plant Health and Welfare.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Secure food supply**  
  **Outcome owners:** Charlotte Baker & Tessa Jones, Directors Agri-Food Chain.  
  **Note:** This outcome contains targets that are part of the Environmental Improvement Plan.

- **Flourishing rural communities**  
  **Outcome owner:** Edward Barker, Director Strategy, Governance and Climate.  
  *(No Environmental Improvement Plan note in the supplied text.)*

---

## Analysis — owner content

### Coverage

- **Secretary of State priorities 1–4:** Every outcome has at least one named owner (or joint owners in priority 3, food sector).
- **Resilience and Security:** All ten outcomes have named owner(s). Nine include the standard **Environmental Improvement Plan (EIP)** note; **Flourishing rural communities** does not in the supplied text.

### Joint / plural ownership

- **Priority 3 — food sector outcome:** Charlotte Baker and Tessa Jones share **Directors Agri-Food Chain** (labelled “Outcome owners” in the source).
- **Resilience — secure food supply:** Same joint pairing and directorate as above.

These are modelled in JSON as an **`owners` array** (two people, same role string) so the HTML can list both names accessibly.

### Directors appearing on multiple outcomes

| Name | Role (as given) | Appears on |
|------|-----------------|------------|
| Edward Barker | Director Strategy, Governance and Climate | SoS priority 1 (one outcome); resilience: lower GHG, climate adaptation, flourishing rural communities |
| Toby Nation | Director Environmental Quality, Infrastructure and Planning | SoS priority 1 (housing); resilience: protection from pollution and environmental hazards |
| David Hallam | Director Floods and Water | SoS priority 2 (both outcomes) |
| Charlotte Baker & Tessa Jones | Directors Agri-Food Chain | SoS priority 3 (food sector outcome); resilience: secure food supply |
| Anjali Juneja | Director Animal and Plant Health and Welfare | Resilience: robust biosecurity; good animal welfare |

This shows **cross-cutting accountability** (strategy/climate, agri-food, animal health) across SoS delivery and resilience tiers.

### EIP pattern

- **Priority 1:** EIP note on three of four outcomes; **housing / infrastructure** outcome has no EIP note in the reference text (matches structured `eip` flags).
- **Priorities 3 (both outcomes):** EIP noted.
- **Priority 4:** No EIP sentences in the reference text for either outcome.
- **Resilience:** EIP on nine outcomes; **Flourishing rural communities** omitted.

### Source quirks (preserved in meaning, normalised in data)

- **“Outcome owners”** vs **“Outcome owner”** — purely grammatical; storage uses singular **“Outcome owner”** in the UI unless two people are listed (**“Outcome owners”** then used in the template).
- **“Outcomes owner”** (waste outcome) — treated as a typo for **Outcome owner**.
- **Emergency preparedness `&`** — stored as **“and”** in JSON for consistency with other copy (screen readers and style).

### Framing text

The reference extract does **not** repeat the longer **Resilience and Security** intro paragraph used elsewhere in the prototype; that paragraph remains in `outcomes.json` and the main `defra-outcomes-framework.md` unless you replace it from an official Defra page.
