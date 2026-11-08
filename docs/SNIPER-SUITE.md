# Sniper Suite — design notes

[Full case study](https://portfolio.jordanmcdonley.com/case-studies/sniper-suite) · [Public support and privacy](https://jordan-sniper-suite.pages.dev/)

**Status: release in progress.** A separate release effort is finishing payment verification and extension publication. This document does not certify Chrome Web Store approval, successful checkout, paid unlock, or payouts.

## The product problem

Researchers repeatedly collect visible page information, compare it, and export a working list. Etsy tags, Maps business listings, Amazon reviews, and Meta ad cards expose different fields. The suite separates those jobs into TagSniper, LeadSniper, ReviewSniper, and AdSniper rather than pretending one generic extractor fits every site.

## Decisions and tradeoffs

| Decision | Why | Consequence |
| --- | --- | --- |
| One task per extension | Controls and outputs can match the site-specific research job. | Four products need individual compatibility and release checks. |
| Shared interface patterns | Keep the suite coherent and make familiar actions reusable. | Shared design must not obscure differences in each site’s data. |
| Accessible-page data | Ground collection in fields the browser can read. | Authentication, device checks, pagination, and DOM changes can limit completeness. |
| Local research lists and exports | Make the collected sample useful outside the immediate page. | Users still need to validate records and handle exports appropriately. |
| Worker bridge for billing/provider state | Separate the page-facing product interface from entitlement checks and billing requests. | Checkout, unlock persistence, restoration, and billing management need distinct tests. |
| Controlled fixtures plus live checks | Fixtures make scenarios repeatable; live checks exercise actual platform behavior. | A fixture or mock cannot establish full marketplace coverage or a real purchase. |

## Product-specific interpretation

- TagSniper: exposed tags and related terms are not guaranteed to be a listing’s complete seller tag set.
- LeadSniper: a missing website link means it was not shown, not that no website exists.
- ReviewSniper: recurring phrases describe the collected sample, not a statistical defect rate for every customer.
- AdSniper: displayed ad age is not evidence of profitability or conversion performance.

## Evidence and ownership

The source documents four Manifest V3 extensions, product-specific tests, packaging, and release materials. The portfolio currently includes a product illustration and an actual Chrome QA capture on fictional listings. These are explicitly distinguished from final live-marketplace and paid-checkout evidence.

Jordan defined the product direction and research workflows; implementation is AI-assisted. Release and billing work is owned by the separate ongoing release effort and was not modified for this portfolio update. Verified store links and current live-use screenshots should replace interim evidence when available.

These notes explain implementation decisions retrospectively. They do not publish private source, customer information, billing credentials, or revenue claims.
