# Buying verified progress in autonomous research

**Fei Yang · Machine economics research note · 11 October 2026**

**Question.** When should a research budget buy more autonomous search, and when should it buy more independent evaluation or physical experiments?

My working judgment is that the answer depends on the conversion from generated candidates to results that support a specified decision. A falling price per agent-hour can coexist with a rising cost per usable result. This note separates reported evidence, arithmetic, and a hypothesis that still needs a field test.

## Evidence checked against primary sources

1. Anthropic reports roughly **$18,000 of compute/API spend over 800 cumulative agent-hours**, with a weak-to-strong research result reaching **PGR 0.97**. Its production-scale transfer attempt produced **+0.5 point, within the noise floor**. The authors also describe adaptive evaluation and reward hacking. These are the authors' results, not a replication by me. [Official report](https://alignment.anthropic.com/2026/automated-w2s-researcher/).

2. The current A-Lab paper reports **353 experiments in 17 days and 36 realized targets out of 57**. This is synthesis evidence, not commercial deployment. [Current article](https://www.nature.com/articles/s41586-023-06734-w). The January 2026 correction clarifies that novelty meant new to the prediction platform, not necessarily new to science; four of forty reexamined reported successes were inconclusive, and one training-data compound was removed. [Author correction](https://www.nature.com/articles/s41586-025-09992-y).

3. Sakana's workshop experiment submitted three selected AI-generated papers; one cleared the reported reviewer-score threshold. The papers were withdrawn under the experiment protocol and did not receive an additional meta-review. It is evidence about that review experiment, not three published research outcomes. [Official account](https://sakana.ai/ai-scientist-first-publication/).

These cases have different output units. Manuscripts, benchmark improvement, successful synthesis, independently replicated improvement, and a customer-relevant decision cannot be added into one “research productivity” count.

## What the published numbers let us calculate

$18,000 / 800 = **$22.50 per cumulative agent-hour**. This does not include an identified full cost of setting up the problem, independent replication, or transferring a method to a customer's setting. It is not a price for purchasing one unit of general scientific progress.

353 / 17 = **20.76 experiments per campaign day**; 36 / 57 = **63.16% target realization**. The first figure is observed campaign throughput, not the laboratory's maximum capacity. Neither figure supplies a commercial yield, product-performance gain, energy bill, or investment return.

The economic issue is the boundary of the output. If a buyer needs a generalizable training improvement, repeated gains on an adaptively queried evaluation are an intermediate product. If a buyer needs a usable material, synthesis alone is an intermediate product until purity, device performance, and the intended application are checked. The required next step consumes scarce resources: evaluator time, untouched data, GPU runs, instruments, materials, or customer trials.

## A simple capacity model

Let G be generated candidates in a period; V be available independent verification slots; q be the fraction of checked candidates meeting a predeclared result criterion; cg and cv be generation and verification costs per candidate. Assume a static one-check-per-candidate workflow, equally costly checks, unchanged candidate quality, and no value from unchecked candidates during this period.

Expected verified results = q × min(G, V)

Total measured cost = cg × G + cv × min(G, V)

Cost per expected verified result = total measured cost / expected verified results

This model omits feedback, intelligent selection, experiment dependencies, fixed costs and queue timing. Its purpose is to identify one falsifiable bottleneck, not to estimate any of the cited projects.

**Entirely hypothetical illustration:** q = 0.5, cg = 5, cv = 20, in arbitrary monetary units.

| Allocation | G | V | Cost | Expected verified results | Cost/result |
|---|---:|---:|---:|---:|---:|
| Initial campaign | 40 | 20 | 600 | 10 | 60 |
| Spend another 200 on search | 80 | 20 | 800 | 10 | 80 |
| Spend another 200 on verification | 40 | 30 | 800 | 15 | 53.33 |

The two extensions have the same budget. Verification wins here because its capacity binds and q is fixed. Search can win if more exploration improves the selected candidates, discovers valuable new questions, reduces verification expense, or changes future research. Those possibilities must be measured rather than assumed away.

## A test a research group could actually run

Choose one narrow research task and a stakeholder decision before the run. Reserve a final evaluation that the search agents cannot query. Predeclare the acceptance threshold, including tolerated capability regressions and a resource-cost ceiling where relevant. A carefully verified negative finding may count if the decision is to stop a specific line of work; record it separately from a performance gain.

Compare two equal-cost marginal allocations across randomized, matched research directions: additional search versus additional independent verification. Keep the final reserve untouched during selection. Record all failures and no-output runs, repeated candidates, evaluator queries, monetary spend, evaluator hours, physical experiment slots, time to decision, and the final reproducibility result. Use multiple campaigns and report uncertainty; one lucky search trajectory is insufficient.

The primary outcome is the number of distinct results that meet the predeclared decision criterion under final independent evaluation per total campaign cost. Report compute/API, labor, instruments and materials separately before combining them. Count stakeholder adoption only when the stakeholder actually uses the result.

**Prediction:** in campaigns where a backlog of unverified candidates grows and independent checking capacity is demonstrably saturated, extra checking will deliver more accepted decision-relevant results per marginal budget than extra search, provided candidate quality and checking quality remain comparable.

**Refutation:** extra search produces a larger independently confirmed marginal gain at equal all-in cost; the backlog disappears without more checking; or the supposed bottleneck is actually poor candidate quality or an irrelevant objective. These outcomes would require changing the allocation rule.

## Uncertainties and present limits

No cited source provides the full cost and decision-conversion data needed to estimate this prediction. Independence is difficult: evaluators may share failure modes with generators; hidden data may overlap with prior training; a synthesis characterization may remain ambiguous. Verification can also be automated, changing V and cv. A useful negative result may have high economic value even without a new artifact.

This is an evidence-grounded allocation hypothesis with checked arithmetic. I have not rerun the cited research campaigns or established customer adoption, commercial value, or return on capital. The next evidence needed is a real campaign with separate search, verification and downstream-decision records.

**Method disclosure:** AI tools assisted source discovery, checking and drafting. Primary-source snapshots and the arithmetic are retained locally. No author-reported scientific result has been relabeled as an independently reproduced result.
