# SpareFoot (sparefoot)

SpareFoot is the largest online marketplace for finding and reserving self-storage units, owned by Storable (the same parent that owns the storEDGE and SiteLink property-management systems, cataloged separately at [api-evangelist/storable](https://github.com/api-evangelist/storable)). SpareFoot itself does not publish a developer portal, API reference, or self-serve API keys for third parties to call. Instead, storage facilities' pricing, unit availability, and promotions reach SpareFoot through one-way, partner-gated data-feed integrations built by property-management software vendors - Storable Edge (storEDGE), SiteLink Web Edition, Storable Easy, Self Storage Manager (E-SoftSys), eDOMICO, and DoorSwap - each of which pushes its own facilities' inventory into the marketplace and receives reservation/lead data back. No endpoint list, request/response schema, or authentication scheme for this feed mechanism is publicly documented; a facility operator or software vendor must go through SpareFoot/Storable's integrations team to be onboarded. This entry documents that access model honestly rather than fabricating an API surface.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/sparefoot/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/sparefoot/refs/heads/main/apis.yml)

## Access model

SpareFoot is the consumer-facing marketplace/lead-generation side of the Storable brand family; storEDGE and SiteLink are the property-management-system side, each with its own API already documented in the separate `storable` entry. This entry deliberately does not restate storEDGE/SiteLink API detail - it covers only what SpareFoot itself, as the marketplace, discloses about how data reaches it.

SpareFoot's own support knowledge base ([support.sparefoot.com](https://support.sparefoot.com/)) lists integration articles for six property-management vendors:

- Storable Edge (storEDGE)
- SiteLink Web Edition
- Storable Easy
- Self Storage Manager (E-SoftSys)
- eDOMICO
- DoorSwap

Each article describes, at a marketing level, how that vendor's software "includes a data feed (API)" that syncs facility, unit, pricing, availability, and promotion data into SpareFoot listings and passes reservation/lead data back - but none discloses an endpoint list, schema, base URL, authentication scheme, or rate limit. There is no self-serve API key, no public API reference, and no NDA-gated document to request the way SiteLink's own legacy SOAP API has. Onboarding as an integration partner happens through SpareFoot/Storable's partner integrations team. Because no technical contract is publicly readable, this entry does not list a fabricated `apis:` array - see `review.yml` for the full findings.

## Tags

- Self Storage
- Marketplace
- Storage Unit Listings
- Lead Generation
- Reservations
- Partner Integration
- Data Feed
- Storable
- SiteLink
- storEDGE

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## Pricing

SpareFoot does not sell API or data-feed access as a metered developer product - what's priced is marketplace participation itself. Historically this was sold as "RentPercent" pricing (a percentage of rent collected per verified move-in, billed for the tenant's length of stay), a model third-party sources say is no longer offered to new clients. Current facility agreements are understood to be negotiated cost-per-reservation or percentage-of-rent arrangements set directly with SpareFoot/Storable sales; no public self-serve price list exists. See `plans/sparefoot-plans-pricing.yml` for sourcing and detail.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/sparefoot)
- [Website](https://www.sparefoot.com/)
- [Documentation](https://support.sparefoot.com/)
- [Plans](plans/sparefoot-plans-pricing.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
