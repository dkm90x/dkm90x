# Acura Atlas — design notes

[Working app](https://atlas.acura.jordanmcdonley.com/) · [Full case study and actual screenshots](https://portfolio.jordanmcdonley.com/case-studies/acura-atlas)

## Problem and approach

Detailed guidance is difficult to use during an appointment or handoff when it is scattered across documents. Atlas organizes sales process, decision support, follow-up, coaching, and governance into a branching reference. The current public app identifies Jordan McDonley as its creator and reports seven areas and 196 indexed entries.

## Decisions and tradeoffs

| Decision | Why | Consequence |
| --- | --- | --- |
| Process-area navigation | A user can begin with the job in front of them instead of remembering a document name. | The taxonomy must be maintained as the reference grows. |
| Expandable entries | Keep nearby stages visible while revealing the detailed reference. | A very long entry can still require scrolling. |
| Search across title, body, and type | Offer a second path when the user knows a term but not its location. | Current literal matching does not supply synonyms or semantic retrieval. |
| Trigger, rationale, review status, and source near the draft | Help distinguish when wording applies and whether it has been approved. | A populated reference is not automatically a current approved policy. |
| Static browser delivery with structured data | Make the reference available through a normal URL and an app-install affordance. | Device installation and offline behavior need separate acceptance checks. |

## Observed evidence

The portfolio review opened Core Sales Process, expanded Stage 3 Discover, searched follow-up, and opened a post-visit message reference. The follow-up search returned 15 results in the checked version. The literal phrase trade appraisal returned none; semantic matching is not implemented. Screenshots show the real app, not invented customer records.

The 196 figure counts indexed entries, not unique procedures. This review did not audit every entry or establish dealership adoption, faster appointments, or sales lift. It did not verify native installation or offline operation.

## Contribution and boundaries

Jordan organized the reference and directed the interface and workflow design; software implementation is AI-assisted. This is an independent sales reference, not official Acura or dealership policy. Brand marks belong to their owners. Drafts and review flags should be checked against current business requirements before operational use.

These notes are retrospective explanations of the current implementation, not a contemporaneous decision log. No private source repository or customer records are distributed here.
