# Debate 2: Can the Epistemic Warranty Become a Real Company?

**Date:** 2026-07-30
**Lineage:** Seeded from Debate 1's joint finding (see `DEBATE.md`): the lucrative artifact in AI is the *epistemic warranty* — per-claim, machine-readable provenance certificates plus an actuarial table of residual risk. This debate tests whether that abstraction survives contact with commercial reality as **one specific company**.
**Goal bar (set by the observer):** not an interesting conclusion — a specific, buildable, defensible, lucrative plan, or an honest kill.

## The Motion

> **"The epistemic-warranty thesis instantiates as a venture-scale company whose wedge is AI legal-citation-and-quote verification — certified filings — expanding to a horizontal claim-certification platform."**

**Debater A** (this session): argues the concrete build.
**Debater B** (independent instance): attacks it — feature-not-company, incumbent bundling, frontier problems — and must counter-propose if it kills the wedge.

A parallel one-shot scout analysis (Debate 2b, see `DEBATE-2B-AI-INSURANCE.md`) independently stress-tests the generalized form: AI-output liability insurance as a market.

---

## Round 1 — Debater A (opening)

**The wedge: AI legal-citation-and-quote verification, sold to litigation firms terrified of Avianca-style sanctions.**

Concretely: a service (API + doc-upload + Word/Clio plugin) that ingests any brief — AI-drafted or human — and tags every case citation, quotation, and factual assertion as **VERIFIED** (byte/pincite-matched against CourtListener + the firm's Westlaw/Lexis seat), **UNSUPPORTED**, **MISQUOTED**, or **MISCITED** (case exists but doesn't stand for the cited proposition — checked by NLI against the actual holding). The output is an auditable certificate attached to the filing.

**Why this wins:**

1. **Willingness to pay is fear-priced.** A single Rule 11 sanction, malpractice claim, or reputational hit dwarfs any subscription; GCs and malpractice insurers will mandate it.
2. **The core check is deterministic and cheap.** Citation existence and quote-matching are byte-level, not model judgment — a below-the-frontier problem (per Debate 1) where we can claim near-zero false "verified" emissions.
3. **Data moat inputs are open.** CourtListener/RECAP is free; existence and quote checks don't require licensing Westlaw's corpus.
4. **It's a wedge, not the whole company.** Once we own "certified filings," the same certificate engine expands to contracts, regulatory filings, medical records, financial disclosures: the horizontal epistemic-warranty platform.

**First customer:** mid-size litigation boutiques and legal-malpractice insurers who'll co-sell.
**First build:** citation extractor + CourtListener existence check + quote byte-matcher — shippable in weeks.

---
