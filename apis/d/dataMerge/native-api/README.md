# DataMerge: Native API Reference

A consolidated summary of DataMerge's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://api.datamerge.ai/docs
- **OpenAPI specification:** https://api.datamerge.ai/schema
- **API base URL:** `https://api.datamerge.ai`

## Authentication

### API Key

Authenticate with your DataMerge API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.datamerge.ai/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.total_pages`. The current page number is read from `pagination.page`.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Items to List](actions/add-items-to-list.md) | `POST /v1/lists/:object_type/:list/add` | [docs](https://api.datamerge.ai/docs) |
| [Create List](actions/create-list.md) | `POST /v1/lists` | [docs](https://api.datamerge.ai/docs) |
| [Delete List](actions/delete-list.md) | `DELETE /v1/lists/:object_type/:list` | [docs](https://api.datamerge.ai/docs) |
| [Enrich Companies](actions/enrich-companies.md) | `POST /v1/company/enrich` | [docs](https://api.datamerge.ai/docs) |
| [Enrich Contacts](actions/enrich-contacts.md) | `POST /v1/contact/enrich` | [docs](https://api.datamerge.ai/docs) |
| [Get Company](actions/get-company.md) | `GET /v1/company/get` | [docs](https://api.datamerge.ai/docs) |
| [Get Company Enrichment Status](actions/get-company-enrichment-status.md) | `GET /v1/company/enrich/:job_id/status` | [docs](https://api.datamerge.ai/docs) |
| [Get Company Hierarchy](actions/get-company-hierarchy.md) | `GET /v1/company/hierarchy` | [docs](https://api.datamerge.ai/docs) |
| [Get Company Webhook Example](actions/get-company-webhook-example.md) | `GET /v1/webhooks/company` | [docs](https://api.datamerge.ai/docs) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contact/get` | [docs](https://api.datamerge.ai/docs) |
| [Get Contact Enrichment Status](actions/get-contact-enrichment-status.md) | `GET /v1/contact/enrich/:job_id/status` | [docs](https://api.datamerge.ai/docs) |
| [Get Contact Search Status](actions/get-contact-search-status.md) | `GET /v1/contact/search/:job_id/status` | [docs](https://api.datamerge.ai/docs) |
| [Get Contact Webhook Example](actions/get-contact-webhook-example.md) | `GET /v1/webhooks/contact` | [docs](https://api.datamerge.ai/docs) |
| [Get Credits Balance](actions/get-credits-balance.md) | `GET /v1/credits/balance` | [docs](https://api.datamerge.ai/docs) |
| [Get List Members](actions/get-list-members.md) | `GET /v1/lists/:object_type/:list` | [docs](https://api.datamerge.ai/docs) |
| [Get Lists](actions/get-lists.md) | `GET /v1/lists` | [docs](https://api.datamerge.ai/docs) |
| [Get Lookalike Company Status](actions/get-lookalike-company-status.md) | `GET /v1/company/lookalike/:job_id/status` | [docs](https://api.datamerge.ai/docs) |
| [Move Item To Another List](actions/move-item-to-another-list.md) | `POST /v1/lists/:object_type/:list/:item_id/move` | [docs](https://api.datamerge.ai/docs) |
| [Remove Item From List](actions/remove-item-from-list.md) | `DELETE /v1/lists/:object_type/:list/:item_id` | [docs](https://api.datamerge.ai/docs) |
| [Search Contacts](actions/search-contacts.md) | `POST /v1/contact/search` | [docs](https://api.datamerge.ai/docs) |
| [Search Lookalike Companies](actions/search-lookalike-companies.md) | `POST /v1/company/lookalike` | [docs](https://api.datamerge.ai/docs) |
