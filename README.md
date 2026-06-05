# EasyPost (easypost)

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
