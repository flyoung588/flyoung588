# What does a successful rebuild actually cost?

Fei Yang · 12 October 2026 · Independent machine-economics source audit

**Question.** When budgeting for a reproducible computational result, should we use the cost of its successful run or the expenditure of reaching that success?

A useful distinction appears in the Reproducible AI List's nanochat campaign. Its published records retain failed cold-rebuild attempts rather than displaying only a passing result. I checked the cost arithmetic and the corresponding certification description; I did not run the workload or verify a cloud invoice.

| Cost boundary | Publisher-reported USD |
|---|---:|
| Successful cold-rebuild attempt | 17.94 |
| Three earlier incomplete or failed certification attempts | 62.37 |
| All four certification attempts | 80.31 |
| Capture and rebuild effort | 96.97 |
| Combined campaign | 177.28 |

The verification campaign cost is **4.48 times** its final successful attempt. Earlier unsuccessful certification attempts account for **77.7%** of certification expenditure. These are ratios calculated from this publisher's estimates, not population estimates. The capture/rebuild total includes unsuccessful setup and instrumentation iterations; it is not a measured autonomous hypothesis-search budget.

**Analysis.** A benchmark's pass cost answers how much a particular successful attempt consumed. A campaign budget asks how much was spent obtaining that pass, including unsuccessful attempts. Using the former as the latter erases costs already recorded in this example. Neither number establishes how much an independent new operator should expect to spend.

For a future measurement of verified progress, I would preserve attempt identity, resource lifetime, unsuccessful outcomes and stopping decisions, alongside the final pass. I would separately report infrastructure expenditure, labour and model/API expenditure. This case supports those accounting distinctions; it does not determine the optimal allocation between research search and verification.

**Refutable judgment.** For comparable cold-rebuild campaigns, a success-only budget will understate realised campaign expenditure whenever unsuccessful attempts incur positive costs. Its usefulness as a predictor can be tested prospectively: freeze each budget estimate before execution, retain every attempt, and compare forecast errors with a budget that includes a retry allowance. A larger retry allowance can also overestimate costs; one retrospective campaign cannot establish which forecast is better.

**Uncertainty.** Costs are publisher estimates, not invoice-backed evidence inspected here. Hardware, tracing versions, setup and stop policies changed across attempts. The source describes a separate certifier and fresh host; this is not independent verification by me or endorsement by an unrelated institution. A successful computational rebuild does not itself validate a scientific claim, and this record does not establish autonomous-science ROI.

**Original evidence.** [Attempt costs](https://github.com/reproducible-ai/notes/blob/b432d885c2e1f4a5327f883d6936b4ac3a6c86ce/024-llm-nanochat/costs.md) · [Cold-rebuild receipt](https://github.com/reproducible-ai/notes/blob/b432d885c2e1f4a5327f883d6936b4ac3a6c86ce/024-llm-nanochat/CERT-TIER2.md) · [Workload record](https://github.com/reproducible-ai/notes/blob/b432d885c2e1f4a5327f883d6936b4ac3a6c86ce/024-llm-nanochat/row.json). Sources read on 12 October 2026 and pinned to commit b432d885c2e1f4a5327f883d6936b4ac3a6c86ce. Source credit: Reproducible AI List / reproducible-ai, [CC BY 4.0](https://github.com/reproducible-ai/notes/blob/b432d885c2e1f4a5327f883d6936b4ac3a6c86ce/LICENSE). This note adds an independent accounting interpretation. Related hypothesis: [Buying verified progress](https://github.com/flyoung588/flyoung588/blob/9e9d56a804a083238f3c08345a92a34326c7c146/research/2026-10-11-verified-progress.md).

Disclosure: AI assisted source checking, arithmetic and writing. No new model inference, cloud workload execution or scientific replication was performed.
