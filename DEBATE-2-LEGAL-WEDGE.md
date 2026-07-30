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

## Round 1 — Debater B (rebuttal and counter-proposal)

Debater A, your wedge is sharp and your fear-pricing instinct is right. But you've built the wrong company, and the reason is instructive: you smuggled the actuarial table out of the warranty thesis and replaced it with a checker. Checkers are commodities. Underwriters are companies. Let me show where this breaks, then hand you the version that survives.

**(i) It's a feature, and the free corpus is an anti-moat.** You cite CourtListener being open and free as a strength. It's the opposite. If the ground truth is public and the core check is byte-level, then your entire differentiated engine is a weekend build that Thomson Reuters, LexisNexis, Harvey, and Microsoft can each replicate in one sprint — and they sit *inside the workflow you have to plug into.* Westlaw already ships KeyCite/Quick Check; Shepard's exists; CoCounsel is bundling citation validation now. Fear-priced demand is real, but it accrues to whoever already holds the Word seat and the Westlaw login, not to a plugin they can extinguish by toggling a feature. "We don't need to license Westlaw's corpus" is not a moat — it's an admission that nothing stops Westlaw from doing this for free tomorrow. A defensible moat has to be data that *compounds and that you alone hold.* You have named none.

**(ii) The deterministic claim is the dishonest part, and it's load-bearing.** Split your four tags. VERIFIED (exists) and MISQUOTED (byte-match) are genuinely deterministic — and genuinely commodity; incumbents give them away. All the *value* lives in MISCITED: the case is real, the quote is real, but it doesn't stand for the proposition. That is exactly the failure that gets lawyers sanctioned, and it is a semantic-entailment judgment — NLI against a holding — which is precisely the above-the-frontier model judgment the epistemic-warranty thesis was invented to escape. So you face a fork: restrict to deterministic checks and sell a commodity, or include MISCITED and emit a "certificate" backed by an unreliable classifier. A certificate on a probabilistic verdict is worthless *unless it carries a calibrated residual-risk number* — the actuarial table. You dropped the table and kept the word "certificate." That's the tell.

**(iii) The horizontal platform is the fantasy, and legal has no feedback oracle.** The entire value of your legal build was one free, structured, authoritative corpus. Contracts, medical records, financial disclosures each have a *different* verification substrate, a different buyer, a different regulator — and most have no open ground-truth corpus at all. The "certificate engine" does not transfer; the corpus was the engine. Worse: legal has no oracle that scores your certificates at scale. A brief's citations are almost never systematically graded against reality, so **you never learn your own false-VERIFIED rate.** Without that feedback loop you can never build an actuarial table, which means you can never honestly warrant anything — you can only assert. A warranty business you can't underwrite is just a checker with a marketing word attached.

**(iv) The correct instantiation: sell certificates only where reality grades them for you.** The warranty does *not* need a deterministic check. It needs a **ground-truth feedback oracle** — a domain where the world returns a verdict on every claim you certified, continuously and at volume. That verdict stream *is* your actuarial table, generated for free, and it's proprietary the moment you're in the loop. That is the compounding, un-copyable moat A is missing.

The vertical that fits best: **AI medical-coding and clinical-documentation assurance — a certificate on every AI-suggested code, priced as denial/audit insurance.** Call it what it is: an underwriter for machine-generated claims.

- **Why the oracle exists:** every claim is adjudicated by a payer. Paid, downcoded, or denied — a labeled outcome on every certificate, every day, across billions of claims. RAC audits and False Claims Act exposure (treble damages) add a second, high-severity label stream. You are handed the exact loss data legal can never obtain.
- **Why it's honestly a warranty:** the underlying "does this code match the documentation" check is probabilistic — fine. You don't sell certainty; you sell a per-code certificate with a calibrated denial/audit probability, backed by your accumulated code→adjudication loss table. That's the actuarial artifact the thesis actually demands.
- **Fear pricing, but recurring and high-ACV:** denials cost U.S. providers hundreds of billions annually; revenue-cycle is a $100B+ market. Unlike a per-brief legal check that fires occasionally at a cheap boutique, this fires on every encounter at every hospital.
- **First customer:** the AI scribe/coding vendors themselves (Abridge, Nuance DAX, Ambience) and large hospital revenue-cycle teams. The AI vendors *need* someone to warrant their output so their buyers will trust it, and they will not build an actuary in-house. You become the liability layer they resell.
- **Why incumbents can't copy fast:** Epic and Optum hold data but sell software and services, not a per-claim underwriting instrument with a calibrated residual-risk table and transferred liability. Building that is an insurance/actuarial motion — culturally and structurally foreign to an EHR vendor and slow to stand up. Your moat is the loss book, and it deepens with every adjudicated claim you touch.
- **First build:** ingest coded encounters + documentation, emit a per-code certificate with a denial-probability score, then *close the loop* by ingesting the 835 remittance/adjudication outcomes and continuously recalibrating.

Keep your certificate primitive. Move it to the one place where the world keeps score — and sell the score, not the check.

---

## Round 2 — Debater A (concession and counter-attack)

**The concession, in full:** the legal wedge is dead as a flagship. The kill shot was not incumbent bundling (survivable) but the feedback-oracle point: nobody systematically grades filed briefs against reality, so the certifier never learns its own false-VERIFIED rate, so there is no actuarial table, so "warranty" is marketing on a checker. Supporting evidence B didn't have: the parallel scout analysis (Debate 2b, run blind) also concluded the capital-light asset is measurement/certification with warranty as packaging, also picked medical coding/RCM, and specified the insurance mechanics (MGA/carrier partner, version-locked models, per-claim and aggregate caps, quarterly re-pricing). Two blind processes converged on B's vertical — which is weak-but-real evidence for the shape, and exactly why it must now be attacked hardest: convergence of two instances of the same model may only mean shared blind spots.

**Attack 1 — The oracle grades the wrong variable.** B has committed A's crime in mirror image: A kept the word "certificate" and dropped the actuarial table; B kept the words "actuarial table" and swapped the graded variable. The 835 remittance stream does not label "code matches documentation." It labels "payer paid, downcoded, or denied" — and payers deny for eligibility, prior auth, timely filing, medical-necessity policy, and contract quirks that have nothing to do with coding correctness; conversely they routinely *pay* miscoded claims. Undercoding is essentially never denied — it is silent revenue loss. Upcoding is frequently paid on submission and clawed back only if audited, 1–3 years later, through a sparse, adversarial channel. So calibrating certificates on adjudication outcomes builds a **payer-behavior model, not a truth model**. Consequences: (a) the "epistemic certificate" quietly becomes a denial-probability score — a real product, but not the warranty thesis; and (b) that product **already exists**: Waystar, Optum, AKASA, Adonis and a crowd of denial-prevention vendors ship denial-probability scoring today. The claimed un-copyable moat — outcome-labeled claims data — is the incumbent exhaust of every clearinghouse in the country.

**Attack 2 — The clearinghouse incumbency.** The entities already in the claim flow — Availity, Waystar, Optum/Change Healthcare — see claims *and* 835s across billions of transactions. The startup's loss book compounds per claim touched; theirs already exists at a scale a startup won't reach in a decade. "They sell software not underwriting" is thin: Waystar already sells denial prevention; a capped warranty is a product decision plus an MGA partnership away. Needed: a structural reason they *can't* follow — conflict of interest, payer-neutrality, channel conflict — or the plan is building their feature for them.

**Attack 3 — The incentive trap, which is also an FCA time bomb.** Who pays the certifier? If providers or AI-coding vendors pay, the certifier is structurally pressured to certify the revenue-maximizing code. Nightmare path: the certificate blesses aggressive coding → payers pay on submission → the loss book records "correct" → the model recalibrates toward aggression → three years later a False Claims Act action with treble damages lands on claims stamped with the certification mark. The warranty didn't miss the tail risk; it *manufactured and concentrated* it. Conversely, a truth-first certifier systematically recommends conservative codes, lowers provider revenue, and churns. So: whose money doesn't corrupt the certificate — payers? at-risk entities? provider compliance offices under DOJ enforcement pressure? Pick, or the thesis dies the same death as legal: a certificate that certifies nothing.

**Demands for Round 3** — no new vertical pivots unless Attack 1 is fatal; converge or kill: (i) the actual ground-truth channel for "code matches documentation" and the honest mix of sparse-truth + dense-proxy calibration; (ii) the structural moat against clearinghouses, or concede the play must be built *with* one (or with a payer) and say what the startup then owns; (iii) the buyer whose incentives align with truth, the pricing unit, and why; (iv) the concrete plan: first 12 months, cold-start data source, MGA/carrier structure, first named-archetype customer and rough ACV, and the 6-month falsification test.

---
