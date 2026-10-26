# Quartzy (quartzy)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Quartzy is a lab management platform for life science teams that combines inventory management, supply ordering, and procurement in one place. Labs track every consumable, reagent, and piece of equipment, submit and approve order requests, and buy from a catalog of millions of lab products. Quartzy exposes a documented public REST API at `api.quartzy.com` so teams can create and update inventory items and order requests from external systems - ELNs, LIMS, and homegrown tools - and subscribe to webhooks for inventory and order-request events. The API is authenticated with a per-user AccessToken (`Access-Token` header) or OAuth2, and is available to all Quartzy accounts.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/quartzy/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/quartzy/refs/heads/main/apis.yml)

## Tags

- Lab Management
- Inventory Management
- Life Sciences
- Procurement
- Ordering
- Laboratory
- Webhooks

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

### Quartzy Inventory Items API

List and filter inventory items in a lab, retrieve a single item with its instances, and update the remaining quantity of an item instance. Items carry type, vendor, catalog number, price, and location metadata; each item can have one or more physical instances that are drawn down as the lab consumes stock.

- **Human URL:** [https://docs.quartzy.com/api/](https://docs.quartzy.com/api/)
- **Base URL:** `https://api.quartzy.com`

#### Tags

- Inventory
- Items
- Instances

#### Properties

- [Documentation](https://docs.quartzy.com/api/)
- [API Reference](https://docs.quartzy.com/api/)
- [OpenAPI](openapi/quartzy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quartzy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quartzy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Quartzy Order Requests API

List and filter order requests for a lab, create new order requests from an external system, retrieve a single request, and advance its status through the Quartzy ordering workflow (new, approved, ordered, received, backordered). This is the primary integration point for pushing procurement out of an ELN or LIMS into Quartzy's ordering and approval flow.

- **Human URL:** [https://docs.quartzy.com/api/](https://docs.quartzy.com/api/)
- **Base URL:** `https://api.quartzy.com`

#### Tags

- Order Requests
- Ordering
- Procurement

#### Properties

- [Documentation](https://docs.quartzy.com/api/)
- [API Reference](https://docs.quartzy.com/api/)
- [OpenAPI](openapi/quartzy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quartzy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quartzy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Quartzy Types API

List and filter the item types (categories such as antibody, chemical, enzyme, or equipment) defined for a lab. Types classify inventory items and order requests and are referenced by their identifier when creating or updating those resources.

- **Human URL:** [https://docs.quartzy.com/api/](https://docs.quartzy.com/api/)
- **Base URL:** `https://api.quartzy.com`

#### Tags

- Types
- Categories
- Metadata

#### Properties

- [Documentation](https://docs.quartzy.com/api/)
- [API Reference](https://docs.quartzy.com/api/)
- [OpenAPI](openapi/quartzy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quartzy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quartzy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Quartzy Labs API

List the labs within an organization and retrieve a single lab. A lab is the organizational and location scope that inventory items, order requests, and types belong to; most inventory and ordering calls are filtered by `lab_id`.

- **Human URL:** [https://docs.quartzy.com/api/](https://docs.quartzy.com/api/)
- **Base URL:** `https://api.quartzy.com`

#### Tags

- Labs
- Locations
- Organizations

#### Properties

- [Documentation](https://docs.quartzy.com/api/)
- [API Reference](https://docs.quartzy.com/api/)
- [OpenAPI](openapi/quartzy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quartzy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quartzy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Quartzy Webhooks API

Register, list, retrieve, and enable or disable webhooks that Quartzy calls when inventory items and order requests change. Webhooks let an external system stay in sync with Quartzy without polling, receiving event payloads as inventory is consumed and order requests move through the approval and ordering workflow.

- **Human URL:** [https://support.quartzy.com/hc/en-us/articles/5333106670747-Quartzy-API-and-Webhooks](https://support.quartzy.com/hc/en-us/articles/5333106670747-Quartzy-API-and-Webhooks)
- **Base URL:** `https://api.quartzy.com`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://docs.quartzy.com/api/)
- [API Reference](https://docs.quartzy.com/api/)
- [OpenAPI](openapi/quartzy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quartzy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quartzy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/quartzy)
- [LinkedIn](https://www.linkedin.com/company/quartzy)
- [Website](https://www.quartzy.com)
- [Documentation](https://docs.quartzy.com/api/)
- [Plans](plans/quartzy-plans-pricing.yml)
- [Rate Limits](rate-limits/quartzy-rate-limits.yml)
- [Fin Ops](finops/quartzy-finops.yml)
- [Support](https://support.quartzy.com/hc/en-us/articles/5333106670747-Quartzy-API-and-Webhooks)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
