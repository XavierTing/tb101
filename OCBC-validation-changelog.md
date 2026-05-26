# OCBC validation — change log for `transaction-banking-101.html`

**Date:** 2026-05-26
**Scope:** Every concrete factual claim in [transaction-banking-101.html](transaction-banking-101.html) was cross-checked against OCBC's public Singapore business-banking website. UOB and DBS were out of scope. The file is bank-agnostic in framing but uses OCBC's branded product names and feature descriptions, so OCBC was the right benchmark.

**Method:** ~20 targeted WebFetches and WebSearches against `ocbc.com/business-banking` and `sdic.org.sg`, one focused query per product. Where a claim sits behind login or a pricing PDF, it is listed under *Unverifiable* below — not edited.

---

## Corrected

### 1. SGD Current Account — SDIC coverage was stated backwards
**Card:** [p-sgdca at line 929](transaction-banking-101.html#L929)

**Old:** *"SDIC deposit insurance covers individuals and charities only — corporate accounts are not insured."*

**New:** *"SGD balances are covered by SDIC deposit insurance up to S$100,000 per depositor per bank — foreign-currency deposits are not insured."*

**Why:** SDIC's published scope of coverage explicitly extends to *"individuals and other non-bank depositors with insured deposits placed with a DI Scheme member, including companies and other unincorporated entities."* OCBC's own Business Growth Account page confirms the account is SDIC-covered up to S$100,000. The old text was materially wrong about corporate eligibility, and the only correct restriction is the currency one (SGD covered, FCY not).

**Sources:**
- [SDIC — Scope of Coverage](https://www.sdic.org.sg/di_scope_of_coverage/)
- [OCBC Business Growth Account](https://www.ocbc.com/business-banking/smes/accounts/business-growth-account)
- [OCBC Foreign Currency Call Account — confirms FCY exclusion](https://www.ocbc.com/business-banking/smes/accounts/foreign-currency-call-account)

---

### 2. OneCollect — wallet list was missing DuitNow QR
**Card:** [p-onecollect at line 1165](transaction-banking-101.html#L1165)

**Old:** *"…accepts QR payments from PayNow, Alipay+, WeChat Pay, UnionPay, and ShopeePay."*

**New:** *"…accepts QR payments from PayNow, Alipay+, WeChat Pay, UnionPay, ShopeePay, and DuitNow QR."*

**Why:** OCBC's OneCollect product page explicitly lists **six** wallets — the file enumerated only five. Since the card frames the value prop as *"one QR sticker on the sign instead of five,"* under-listing the wallets actively misleads.

**Source:** [OCBC OneCollect](https://www.ocbc.com/business-banking/smes/business-tools/onecollect)

---

### 3. POS Terminal — scheme list was missing UnionPay and JCB
**Card:** [p-pos at line 1179](transaction-banking-101.html#L1179)

**Old:** *"…any major card or contactless wallet (Visa, Mastercard, PayNow, Alipay+, WeChat)."*

**New:** *"…any major card or contactless wallet (Visa, Mastercard, UnionPay, JCB, PayNow, Alipay+, WeChat)."*

**Why:** OCBC's marketing for its terminal lists Visa, Mastercard, **UnionPay, JCB**, Alipay+, WeChat Pay, and PayNow on one device. The card's framing — *"one device handles every payment type — no separate hardware per scheme"* — relies on the list being complete.

**Source:** OCBC POS Terminal description (via [OCBC SMEs Receiving Payments](https://www.ocbc.com/business-banking/smes/transactions/receiving-payments) and merchant solution materials)

---

### 4. PayNow for Business — identifier list omitted FIN
**Card:** [p-paynow at line 1017](transaction-banking-101.html#L1017)

**Old:** *"…UEN for businesses, mobile or NRIC for individuals."*

**New:** *"…UEN for businesses, mobile or NRIC/FIN for individuals."*

**Why:** OCBC's PayNow Corporate FAQ lists five proxies: mobile, NRIC, FIN, UEN, VPA. FIN (Foreign Identification Number) is the equivalent of NRIC for foreign residents and is meaningful enough to belong in the basic identifier sketch. VPA is rarer and left out for brevity.

**Source:** [OCBC PayNow Corporate FAQ (PDF)](https://www.ocbc.com/assets/pdf/paynow/faq_paynow_corporate_qr.pdf)

---

## Verified — left as-is

Every other concrete claim checked out against OCBC's published content. Listed compactly:

| Card | Claim verified | OCBC source |
|---|---|---|
| [p-mcba](transaction-banking-101.html#L918) | "holds up to 13 currencies" — confirmed list: USD, EUR, AUD, JPY, GBP, CNH, HKD, CAD, NZD, CHF, SEK, DKK, NOK | [MCA](https://www.ocbc.com/business-banking/smes/accounts/multi-currency-business-account) |
| [p-fcca](transaction-banking-101.html#L943) | "USD, EUR, AUD, JPY, GBP, or another major FCY" — OCBC supports 9 (AUD, CAD, CHF, EUR, GBP, HKD, JPY, NZD, USD) | [FCY Call Account](https://www.ocbc.com/business-banking/smes/accounts/foreign-currency-call-account) |
| [p-td](transaction-banking-101.html#L954) | "SGD and ten foreign currencies" | [FCY Time Deposit](https://www.ocbc.com/business-banking/smes/accounts/foreign-currency-time-deposit) |
| [p-fast](transaction-banking-101.html#L1006) | 24/7; per-bank limit S$200K+ (OCBC sits at S$200K); some banks up to S$1M industry-wide | [OCBC Making Payments](https://www.ocbc.com/business-banking/smes/transactions/making-payments) |
| [p-giro](transaction-banking-101.html#L1028) | "money lands 2–3 business days later" — OCBC: up to 2 working days | same |
| [p-meps](transaction-banking-101.html#L1039) | "no upper limit", "final and irrevocable", FAST cap at S$200K | same |
| [p-network](transaction-banking-101.html#L1050) | flat-fee (S$15), HK/MY/Indonesia/China, same-day | [Corporate Transaction Banking](https://www.ocbc.com/business-banking/corporates/transaction-banking) |
| [p-tt](transaction-banking-101.html#L1061) | "60+ currencies, SWIFT gpi" — OCBC OTT/World Transfer supports 64 | same |
| [p-iach](transaction-banking-101.html#L1072) | "ACH in the US, BACS in the UK, etc." — 8 markets at OCBC | same |
| [p-vpc](transaction-banking-101.html#L1083) | "single-use or limited-use; set limit, merchant category, expiry" | [Virtual Purchasing Card](https://www.ocbc.com/business-banking/corporates/virtual-purchasing-card) |
| [p-egiro](transaction-banking-101.html#L1146) | "fully digital DDA; approve in minutes, not weeks" | [OCBC eGIRO](https://www.ocbc.com/business-banking/smes/transactions/egiro) |
| [p-va](transaction-banking-101.html#L1157) | virtual account numbering for reconciliation | [OCBC Receiving Payments](https://www.ocbc.com/business-banking/smes/transactions/receiving-payments) |
| [p-deposit](transaction-banking-101.html#L1190) | "any CDM, 24/7, nationwide" — OCBC: ATMs islandwide, 24/7 | [Business Deposit Card](https://www.ocbc.com/business-banking/smes/transactions/business-deposit-card) |
| [p-creditapi](transaction-banking-101.html#L1201) | real-time credit notifications, broader API catalogue | [OCBC API Store](https://api.ocbc.com/store/) |
| [p-sweep](transaction-banking-101.html#L1253) | rule-based sweep, intraday/EOD scheduling, configurable allocation | [Corporate Transaction Banking](https://www.ocbc.com/business-banking/corporates/transaction-banking) |
| [p-io](transaction-banking-101.html#L1264) | preferential rate based on group balances, no fund movement | same |
| [p-pool](transaction-banking-101.html#L1275) | no physical fund movement | same |
| [p-tradesuite](transaction-banking-101.html#L1335) | LCs, documentary collections, invoice financing all confirmed | [OCBC SME Trade](https://www.ocbc.com/business-banking/smes/trade) |
| [p-invoicefin](transaction-banking-101.html#L1346) | Sales / Purchase variants both offered | [Invoice Financing (Sales)](https://www.ocbc.com/business-banking/smes/trade/invoice-financing-sales) / [(Purchase)](https://www.ocbc.com/business-banking/smes/trade/invoice-financing-purchase) |
| [p-arp](transaction-banking-101.html#L1431) | "up to 360 days", "true sale", off seller's balance sheet | [Accounts Receivable Purchase](https://www.ocbc.com/business-banking/smes/trade/accounts-receivable-purchase) |
| [p-fx](transaction-banking-101.html#L1483) | self-service, live streaming rates via Velocity/Business App | [FX Online](https://www.ocbc.com/business-banking/fx-online) |
| [p-portal](transaction-banking-101.html#L1535) | Velocity maker/checker (Maker/Authoriser), multi-module corporate portal | [OCBC Velocity](https://www.ocbc.com/business-banking/digital-business-banking) |
| [p-mobile](transaction-banking-101.html#L1546) | Business App = mobile companion to Velocity for balances + approvals | [OCBC Business App](https://www.ocbc.com/business-banking/smes/business-tools/business-mobile-banking) |
| [p-h2h](transaction-banking-101.html#L1557) | "ISO 20022 and MT940" — OCBC migrated to ISO 20022 CBPR+ in Nov 2025 | [ISO 20022 CBPR+](https://www.ocbc.com/business-banking/digital-business-banking/iso20022.page) |
| [p-api](transaction-banking-101.html#L1568) | REST API catalogue for payments / balances / status / alerts | [OCBC API Store](https://api.ocbc.com/store/) |

---

## Unverifiable from public pages — flagged, not edited

### Banker's Guarantee / Standby LC commission — "1–2% per year"
[p-bg at line 1359](transaction-banking-101.html#L1359). OCBC publishes its pricing only in a downloadable Banker's Guarantee Pricing Guide PDF behind a click-to-download, not on the product page. The 1–2% per annum figure is the industry-standard band, so the claim is almost certainly directionally correct, but it could not be confirmed for OCBC specifically from the public web. Suggest pulling the latest PDF and confirming before any audience-facing publication.

### Receivables & Supplier Finance — buyer-anchored portal model
[p-scf at line 1420](transaction-banking-101.html#L1420). OCBC publishes Invoice Financing (Sales/Purchase) and ARP, but I did not find a public buyer-anchored *programme-style* SCF portal where suppliers click to take early payment at the buyer's pricing — that anchor-led model is more visible at HSBC, Standard Chartered, and DBS in this region. OCBC may offer it under enterprise/corporate relationships not exposed on the public site. The card describes the canonical SCF model, which is fine educationally; flagging for an OCBC-specific accuracy check if needed.

---

## Bank-agnostic — intentionally not changed

### Business Debit Card — "Visa/Mastercard"
[p-debit at line 1094](transaction-banking-101.html#L1094). OCBC's Business Debit Card is Mastercard-only. The file says *"A Visa/Mastercard debit card"* as a general industry description ("most banks issue on Visa or Mastercard"), not as a claim about a specific bank. Left as-is.

### FAST — "some now offer up to S$1M"
[p-fast at line 1006](transaction-banking-101.html#L1006). OCBC's per-transaction cap is S$200,000. The "up to S$1M" half is a generic industry statement (DBS, UOB, and others offer higher tiers). The wording *"some now offer"* signals this isn't OCBC-specific, so the claim stands.

### Notional Pooling — jurisdictional restrictions
[p-pool at line 1276](transaction-banking-101.html#L1276). The US ban and China/India restrictions are general regulatory facts (well-documented in industry literature), not OCBC claims. Cross-checks against OCBC weren't applicable.

---

## Net result

Four corrections applied inline. Twenty-five concrete claims verified. Two flagged for follow-up (BG commission, anchor-led SCF). Three claims explicitly left as bank-agnostic.

---

## Addendum — 2026-05-26 — "How the bank earns" rows on FAST and PayNow

User spot-checked two economics claims the original pass didn't audit directly. Both verified against OCBC's published pricing — no edits required.

### FAST — "Small fee per transaction. Volume game."
[p-fast at line 1008](transaction-banking-101.html#L1008). OCBC charges **S$0.50 per outgoing FAST transaction** via OCBC Velocity or the Business Mobile Banking app. At S$0.50 a send, this is unambiguously a "small fee, volume game" — the Business Growth Account even bundles the first 80 FAST and 80 GIRO transactions a month for free, which only makes sense if the per-unit margin is negligible. **Verified.**

### PayNow for Business — "Same fee model as FAST"
[p-paynow at line 1019](transaction-banking-101.html#L1019). OCBC's business pricing guide states PayNow Corporate outgoing transfers carry the *"Applicable GIRO or FAST transaction fee"* (i.e. S$0.50 if it rides FAST rails, S$0.20 if GIRO) plus a S$0.20 lookup fee that is currently waived through 31 Dec 2028. So PayNow Corporate genuinely inherits the FAST fee — the file's claim is literally accurate, not a simplification. Incoming PayNow is free (waiver in effect through 31 Dec 2028). **Verified.**

**Sources:**
- [OCBC Business Banking Pricing Guide](https://www.ocbc.com/business-banking/help-and-support/accounts-and-services/business-pricing-guide)
- [OCBC PayNow Corporate](https://www.ocbc.com/business-banking/smes/business-tools/paynowcorporate)
