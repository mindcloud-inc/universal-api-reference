# Sponsy: Native API Reference

A consolidated summary of Sponsy's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.getsponsy.com
- **API base URL:** `https://api.getsponsy.com`

## Authentication

### API Key

Primary Sponsy API key authentication using the X-Api-Key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://getsponsy.com/blog/zapier-integration-with-sponsy)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `cursor.afterCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `afterCursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `orderDirection`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 350 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /v1/customers` | [docs](https://docs.getsponsy.com/CRM-182b5594716880bd9d7afde179bc1114) |
| [Create Publication Slot](actions/create-publication-slot.md) | `POST /v1/publications/:publicationId/slots` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [Create Tag](actions/create-tag.md) | `POST /v1/tags` | [docs](https://docs.getsponsy.com/Workspace-Settings-10bb5594716880348de9ce02c29f53f0) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /v1/customers/:customerId` | [docs](https://docs.getsponsy.com/CRM-182b5594716880bd9d7afde179bc1114) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /v1/tags/:tagId` | [docs](https://docs.getsponsy.com/Workspace-Settings-10bb5594716880348de9ce02c29f53f0) |
| [Get Customer](actions/get-customer.md) | `GET /v1/customers/:customerId` | [docs](https://docs.getsponsy.com/CRM-182b5594716880bd9d7afde179bc1114) |
| [Get Customer Metrics](actions/get-customer-metrics.md) | `GET /v1/customers/:customerId/metrics` | [docs](https://docs.getsponsy.com/Customer-Portal-184b55947168803c9d21cca09e49f22b) |
| [Get Publication](actions/get-publication.md) | `GET /v1/publications/:publicationId` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [Get Publication Placement](actions/get-publication-placement.md) | `GET /v1/publications/:publicationId/placements/:placementId` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [Get Publication Slot](actions/get-publication-slot.md) | `GET /v1/publications/:publicationId/slots/:slotId` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [Get Publication Status](actions/get-publication-status.md) | `GET /v1/publications/:publicationId/status/:statusId` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [Get Tag](actions/get-tag.md) | `GET /v1/tags/:tagId` | [docs](https://docs.getsponsy.com/Workspace-Settings-10bb5594716880348de9ce02c29f53f0) |
| [List Customer Contacts](actions/list-customer-contacts.md) | `GET /v1/customers/:customerId/contacts` | [docs](https://docs.getsponsy.com/Customer-Portal-184b55947168803c9d21cca09e49f22b) |
| [List Customer Slots](actions/list-customer-slots.md) | `GET /v1/customers/:customerId/slots` | [docs](https://docs.getsponsy.com/Customer-Portal-184b55947168803c9d21cca09e49f22b) |
| [List Customers](actions/list-customers.md) | `GET /v1/customers` | [docs](https://docs.getsponsy.com/CRM-182b5594716880bd9d7afde179bc1114) |
| [List Publication Placements](actions/list-publication-placements.md) | `GET /v1/publications/:publicationId/placements` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [List Publication Slots](actions/list-publication-slots.md) | `GET /v1/publications/:publicationId/slots` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [List Publication Statuses](actions/list-publication-statuses.md) | `GET /v1/publications/:publicationId/status` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [List Publications](actions/list-publications.md) | `GET /v1/publications` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [List Tags](actions/list-tags.md) | `GET /v1/tags` | [docs](https://docs.getsponsy.com/Workspace-Settings-10bb5594716880348de9ce02c29f53f0) |
| [Update Customer](actions/update-customer.md) | `PATCH /v1/customers/:customerId` | [docs](https://docs.getsponsy.com/CRM-182b5594716880bd9d7afde179bc1114) |
| [Update Publication Slot Price](actions/update-publication-slot-price.md) | `PATCH /v1/publications/:publicationId/slots/:slotId` | [docs](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e) |
| [Update Tag](actions/update-tag.md) | `PATCH /v1/tags/:tagId` | [docs](https://docs.getsponsy.com/Workspace-Settings-10bb5594716880348de9ce02c29f53f0) |
