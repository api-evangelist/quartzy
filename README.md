# Quartzy (quartzy)

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
