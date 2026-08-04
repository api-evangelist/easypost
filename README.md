# EasyPost (easypost)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

EasyPost is a multi-carrier shipping API platform for the United States and international markets. It exposes a REST API spanning shipments, rating, labels, tracking, addresses, parcels, insurance, claims, pickups, scan forms, refunds, batches, end-shippers, reports, customs info, carrier accounts, and webhooks. EasyPost integrates 100+ carriers including USPS, UPS, FedEx, DHL, Canada Post, and Royal Mail.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/easypost/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/easypost/refs/heads/main/apis.yml)

## Tags

- Shipping
- Logistics
- Multi-Carrier
- Tracking
- Labels
- Insurance

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-30

## APIs

### EasyPost Shipping API

Core REST API. Resources: Shipments (immutable; ship + buy rate), Rates, Addresses, Parcels, CustomsInfo, Forms, Labels (PNG/PDF/ZPL/EPL2), Pickups, ScanForms, Refunds, Batches, EndShippers, CarrierAccounts. Authentication uses your API key as HTTP Basic auth username (EASYPOST_API_KEY). Test and Production keys are issued separately.

- **Human URL:** [https://docs.easypost.com/docs/shipments](https://docs.easypost.com/docs/shipments)
- **Base URL:** `https://api.easypost.com/v2`

#### Tags

- Shipments
- Rates
- Labels
- Addresses
- Pickups
- Refunds

#### Properties

- [Documentation](https://docs.easypost.com/)
- [Authentication](https://docs.easypost.com/docs/authentication)
- [Postman Collection](collections/easypost.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/easypost.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### EasyPost Tracking API

Standalone Tracking API: create Trackers from a tracking code + carrier, receive webhooks on status changes, query historical scan events. Standard Tracking and Advanced Tracking tiers are available with different per-shipment pricing.

- **Human URL:** [https://docs.easypost.com/docs/trackers](https://docs.easypost.com/docs/trackers)
- **Base URL:** `https://api.easypost.com/v2`

#### Tags

- Tracking
- Webhooks

#### Properties

- [Documentation](https://docs.easypost.com/docs/trackers)
- [Postman Collection](collections/easypost.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/easypost.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### EasyPost Webhooks API

Asynchronous Event delivery surface. EasyPost POSTs Event objects to subscriber URLs whenever asynchronous objects (batches, trackers, scan forms, refunds, reports, payments, claims, insurance, shipment invoices) change state. Each delivery is signed with an HMAC-SHA256 signature in the X-Hmac-Signature header, derived from a per-webhook secret. Subscribers must return a 2XX status code; non-2XX responses are retried.

- **Human URL:** [https://docs.easypost.com/docs/webhooks](https://docs.easypost.com/docs/webhooks)
- **Base URL:** `https://api.easypost.com/v2`

#### Tags

- Webhooks
- Events
- AsyncAPI
- HMAC

#### Properties

- [Documentation](https://docs.easypost.com/docs/webhooks)
- [Events](https://docs.easypost.com/docs/events)
- [Payloads](https://docs.easypost.com/docs/events/payloads)
- [AsyncAPI](asyncapi/easypost-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/easypost.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/easypost.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### EasyPost Insurance & Claims API

Insurance API: insure shipments at 1% of declared value with a $1 minimum. Claims API: file and manage damage/loss/theft claims via REST.

- **Human URL:** [https://docs.easypost.com/docs/insurance](https://docs.easypost.com/docs/insurance)
- **Base URL:** `https://api.easypost.com/v2`

#### Tags

- Insurance
- Claims

#### Properties

- [Documentation](https://docs.easypost.com/docs/insurance)
- [Postman Collection](collections/easypost.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/easypost.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### EasyPost Reports API

Generate Shipment, Tracker, Refund, Payment Log, and other reports asynchronously; download CSVs from the URL returned in the report object.

- **Human URL:** [https://docs.easypost.com/docs/reports](https://docs.easypost.com/docs/reports)
- **Base URL:** `https://api.easypost.com/v2`

#### Tags

- Reports
- Reconciliation

#### Properties

- [Documentation](https://docs.easypost.com/docs/reports)
- [Postman Collection](collections/easypost.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/easypost.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/easypost)
- [LinkedIn](https://www.linkedin.com/company/easypost)
- [Website](https://www.easypost.com/)
- [Developer Portal](https://docs.easypost.com/)
- [Plans](plans/easypost-plans-pricing.yml)
- [Rate Limits](rate-limits/easypost-rate-limits.yml)
- [Fin Ops](finops/easypost-finops.yml)
- [Integrations](https://www.easypost.com/partners/)
- [L L Ms Txt](https://docs.easypost.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
