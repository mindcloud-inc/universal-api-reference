# Momence: Native API Reference

A consolidated summary of Momence's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://api.docs.momence.com
- **OpenAPI specification:** https://static.momence.com/schema/api-v2-schema.yaml
- **API base URL:** `https://momence.com/_api/primary/api/v1`

## Authentication

### Custom

Momence legacy host-scoped API token passed as query params hostId and token.

### Credentials

- **Host ID:** `hostId` · required · Momence host account identifier sent as the hostId query parameter.
- **Token:** `token` · required · Legacy Momence API token sent as the token query parameter.

[Official authentication documentation](https://api.docs.momence.com/reference/api-reference)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | `GET /Customers` | [docs](https://api.docs.momence.com/reference/api-reference) |
| [List Events](actions/list-events.md) | `GET /Events` | [docs](https://api.docs.momence.com/reference/api-reference) |
| [List Memberships](actions/list-memberships.md) | `GET /Memberships` | [docs](https://api.docs.momence.com/reference/api-reference) |
| [List Products](actions/list-products.md) | `GET /Products` | [docs](https://api.docs.momence.com/reference/api-reference) |
