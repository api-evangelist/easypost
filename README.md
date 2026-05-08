# EasyPost (easypost)

EasyPost is a multi-carrier shipping API platform for the United States and international markets. It exposes a REST API spanning shipments, rating, labels, tracking, addresses, parcels, insurance, claims, pickups, scan forms, refunds, batches, end-shippers, reports, customs info, carrier accounts, and webhooks. EasyPost integrates 100+ carriers including USPS, UPS, FedEx, DHL, Canada Post, and Royal Mail.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/easypost/refs/heads/main/apis.yml)

## Type
- **x-type:** company

## Tags
- Shipping, Logistics, Multi-Carrier, Tracking, Labels, Insurance

## Timestamps
- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

### EasyPost Shipping API
Core REST API. Resources: Shipments (immutable; ship + buy rate), Rates, Addresses, Parcels, CustomsInfo, Forms, Labels (PNG/PDF/ZPL/EPL2), Pickups, ScanForms, Refunds, Batches, EndShippers, CarrierAccounts. Authentication uses your API key as HTTP Basic auth username (EASYPOST_API_KEY). Test and Production keys are issued separately.
- **Base URL:** `https://api.easypost.com/v2`
- **Docs:** https://docs.easypost.com/

### EasyPost Tracking API
Standalone Tracking API: create Trackers from a tracking code + carrier, receive webhooks on status changes, query historical scan events. Standard Tracking and Advanced Tracking tiers are available with different per-shipment pricing.
- **Base URL:** `https://api.easypost.com/v2`
- **Docs:** https://docs.easypost.com/docs/trackers

### EasyPost Insurance & Claims API
Insurance API: insure shipments at 1% of declared value with a $1 minimum. Claims API: file and manage damage/loss/theft claims via REST.
- **Base URL:** `https://api.easypost.com/v2`
- **Docs:** https://docs.easypost.com/docs/insurance

### EasyPost Reports API
Generate Shipment, Tracker, Refund, Payment Log, and other reports asynchronously; download CSVs from the URL returned in the report object.
- **Base URL:** `https://api.easypost.com/v2`
- **Docs:** https://docs.easypost.com/docs/reports

## Common Properties
- [Website](https://www.easypost.com/)
- [Developer Portal](https://docs.easypost.com/)
- [Plans](plans/easypost-plans-pricing.yml) — reconciled (free Wallet up to 3K/mo; BYOA $20/mo + per-label; metered tracking/insurance)
- [RateLimits](rate-limits/easypost-rate-limits.yml) — reconciled (per-account; tens of RPS baseline)
- [FinOps](finops/easypost-finops.yml) — reconciled (FOCUS-aligned)

## Maintainers
**FN:** Kin Lane

**Email:** kin@apievangelist.com
