# Same product, privacy lens

> **How you'll submit this lab**
>
> This repo is your lab. Fork it, do the work described below in your fork, then open a pull
> request back into this repository. An AI reviewer will check your PR against `rubric.md` and
> leave feedback directly on the PR. See `README.md` for the full workflow.

Complete **[GDPR and the EU Data & Privacy Stack](../content/01_gdpr-fundamentals.md)** before starting this lab.

## Lesson alignment

- **Learning objectives:** By the end, you can **complete** a mini GDPR audit for a real-world AI scenario and **write** a short client recommendation memo that identifies obligations, residual risks, and required next steps.
- **Lesson setup requirements:** Revisit the lesson sections on `controllers vs processors`, `lawful bases`, `purpose limitation`, `data subject rights`, `DPIA triggers`, `international transfers`, and `stacking with AI Act and ePrivacy`.

---

## Submission hygiene

- **Filenames:** Use clear, descriptive names (avoid vague names such as `lab.docx` or `audit_final.pdf`).
- **Scope:** Your **GitHub** repository must contain **only materials for this lab**—no unrelated projects, dumps, or personal files.
- **README:** In your GitHub repository, use `README.md` to list each submitted file and what it contains.

**GitHub only:** Submit the URL to a **GitHub repository** that contains everything for this lab (Markdown, code, exports, images, decks). Do **not** submit a standalone Google Doc, Notion page, or cloud-only link as your primary deliverable—put sources or exports (for example `.md`, `.pdf`, `.pptx`, screenshots) **in the repository**.

## Kick-off

### Your scenario choice

**Option A — Continue with your EU AI Act partner and project.**  
If you worked on the EU AI Act lab with a partner, you may carry the same scenario forward. Pick the one case from that lab most likely to involve personal data (usually the high-risk or prohibited case). You will now run a GDPR audit on the same system you already mapped through AI Act risk tiers. This is a realistic consulting pattern: AI Act and GDPR analysis often happen in parallel, not in sequence.

**Option B — Start fresh with a new scenario.**  
If you prefer a different context, pick one of the following:

- **(a) Fine-tune an LLM on support chat logs** — a B2B SaaS company wants to train a customer-service model on two years of live support conversations, including names, email addresses, and complaint content.
- **(b) CV screening with human review** — an HR tech startup sells a tool that ranks job applicants using structured and unstructured resume data, with a recruiter confirming or overriding the shortlist.
- **(c) E-commerce personalisation with analytics cookies** — a mid-size retailer wants to run a recommendation engine using first-party cookie data and purchase history, with a US-based analytics vendor in the stack.

Either way, **commit to one scenario before moving forward**. Mixed or hypothetical fact patterns produce weak audit work.

### Setup / first run

1. Open a blank working document titled `GDPR Audit Pack - YourName`.
2. Split the document into two sections: `Audit worksheet` and `Client recommendation memo`.
3. Write a **fact pattern paragraph** (five to eight lines) covering: who the client is, what personal data is involved, which geography the data subjects are in, whether a US or non-EU vendor is in the stack, and what the AI system is supposed to do.
4. Share the fact pattern with your partner so both of you are working from the same common ground.

### Expected output of first step

A shared, written fact pattern that your partner could read and immediately identify: what data is flowing, to whom, and for what purpose. You will build the rest of the audit on top of this.

---

## CFU checkpoints

### 1. Recognize

Read your fact pattern back and identify: which categories of personal data are present, whether any special-category data (Article 9) might be inferred or included, and whether the data flow crosses an EU border at any point.

### 2. Apply

Complete the full audit worksheet (Sections A, B, and C below) for your scenario. For every lawful basis you propose, write a one-line justification. If you are unsure, write `TBD — legal review` rather than guessing.

### 3. Integrate

Write the client recommendation memo. It should reflect the audit findings and include a bottom-line recommendation (go / go with conditions / stop), the top three actions the client must take, and the residual risks you are disclosing even if the project proceeds.

### 4. Verify

Swap your recommendation memo with your partner. Use the peer feedback rubric below. The reviewer acts as the client: they can accept the recommendation, challenge one finding, or ask for a redesign of one section.

### 5. Debrief

After the swap, compare notes. Where did the two audits agree on lawful basis or DPIA need? Where did they diverge? For divergences, agree on which reading is stronger and why.

---

## Core

### Phase 1: Build the fact pattern

If you are continuing from the EU AI Act lab, write a brief **transition note** at the top of your document: which case you are carrying forward, what AI Act tier it fell into, and why it is the most interesting case for GDPR purposes. This one paragraph keeps the two audits connected and mirrors what a real engagement team would document.

If you are starting fresh, write your fact pattern from scratch using the kick-off instructions above.

Either way, your fact pattern must answer:

- Who is the client? (company type, industry, approximate size)
- What personal data is processed? (categories, volume, sensitivity)
- Who are the data subjects? (employees, customers, applicants, the public)
- Where are the data subjects located? (EU/EEA, third countries, or mixed)
- Who are the vendors in the stack? (especially non-EU processors)
- What does the AI system actually do with the data?
- Is there any automated decision-making with legal or similarly significant effects?

### Phase 2: Mini GDPR audit worksheet

Work through each section below in your document. Be specific — vague answers are not useful in a real client audit.

#### Section A — Data map

| Field | Your answer |
|---|---|
| Categories of personal data | |
| Sources (where data comes from) | |
| Purpose(s) — one row per purpose | |
| Lawful basis per purpose — or `TBD — legal review` | |
| Retention period per purpose | |
| Recipients and sub-processors | |
| International transfers and transfer mechanism | |

For the lawful basis column, use the six options from Article 6: consent, contract, legal obligation, vital interests, public task, or legitimate interests. If you are considering legitimate interests (LIA), note the three-step test: purpose, necessity, balancing.

#### Section B — Risk and rights

Answer each question in one to three sentences:

- Are any special-category data present or inferable from the outputs (Article 9)?
- Is there automated decision-making with legal or similarly significant effects (Article 22)? If yes, what safeguard applies?
- Is a DPIA required? Use the EDPB's nine criteria: explain which apply and why.
- What data subject friction points are most likely? (Most commonly: right of access, right to erasure, right to object to profiling)
- What is the controller / processor split? Name each entity and its role.
- Is a DPA (Data Processing Agreement) needed with any vendor? Which ones?

#### Section C — Law stacking (one line each)

- **AI Act cross-check:** What tier did the AI system fall into (or would you hypothesize)? Does the AI Act add any obligation that GDPR does not cover?
- **ePrivacy check:** Does the scenario involve cookies, tracking pixels, or device-level data? If yes, does ePrivacy's consent requirement override GDPR's flexibility?
- **Data Act check:** Is there connected product or cloud switching data involved? (Usually N/A for most AI scenarios — but flag it if your scenario touches IoT or infrastructure.)

### Phase 3: Write the client recommendation memo

Write **300–400 words** addressed to your client. Write it as if you are a consultant delivering a short advisory note, not as if you are filling in a worksheet.

Your memo must include:

- **Bottom line:** go / go with conditions / stop — and the one-sentence reason.
- **Top three actions:** specific, concrete, and sequenced. For example: `(1) Establish a DPA with [vendor] before any data flows; (2) conduct a DPIA before first processing; (3) revise the privacy notice to cover [specific new purpose].`
- **Residual risks:** two to three risks that remain even if the client follows your recommendations. Be honest — clients need to know what cannot be fully eliminated.

Avoid academic language. Write as if you are handing this note to the client's legal team or CTO and they have five minutes to read it.

### Phase 4: Partner swap and peer review

Swap your recommendation memo with your partner. Use this rubric when reviewing:

| Criterion | Score 1–3 | Comment |
|---|---|---|
| Clear bottom-line recommendation | | |
| Lawful basis selection is justified | | |
| Top actions are specific and sequenced | | |
| Residual risks are named honestly | | |
| Law stacking is addressed (AI Act / ePrivacy) | | |

After the rubric, write two to three sentences as the "client": either accept the recommendation, flag one concern, or ask the consultant to rethink one section.

---

## Reinforce

If you finish early, push the depth of your audit:

- Add a **DPIA outline** for the most sensitive processing activity. You do not need to write a full DPIA — just map the main sections: description of processing, necessity and proportionality assessment, risk identification, and proposed mitigation.
- Identify **one specific clause** you would want to see in the DPA with the main vendor and explain why.
- Rewrite your bottom-line recommendation as if the client just told you they also serve data subjects in the UK. Does anything change under UK GDPR?

---

## Stretch

Take the highest-risk processing activity in your scenario and build a **mini data protection by design checklist** for it. For each item, note whether the client's current setup passes, fails, or is unknown:

- Data minimisation: is only the minimum necessary data collected?
- Purpose binding: is the data technically restricted to the stated purpose?
- Access controls: is access limited to those who need it?
- Retention enforcement: are there automated deletion or anonymisation policies?
- Subject rights workflow: can the client respond to an access or erasure request within the 30-day deadline?
- Incident response: is there a documented process to detect and notify a breach within 72 hours?

Keep this to half a page. The goal is better consulting depth, not a second full memo.
