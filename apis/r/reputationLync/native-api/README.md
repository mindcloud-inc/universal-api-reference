# ReputationLync: Native API Reference

A consolidated summary of ReputationLync's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/25361963/2s93Xzw2bS
- **API base URL:** `https://reputationlync.com/app/api/customer`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/25361963/2s93Xzw2bS#d29ae242-4854-443e-8610-ee1403ab793b)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Customer](actions/add-customer.md) | `POST /addCustomer` | [docs](https://documenter.getpostman.com/view/25361963/2s93Xzw2bS#46718236-5ef1-4c93-992d-cd7d3722b02f) |
| [List Customers](actions/list-customers.md) | `POST /listCustomer` | [docs](https://documenter.getpostman.com/view/25361963/2s93Xzw2bS#5c16a301-9417-4539-b9c5-dcdf666159ff) |
| [Validate API Key](actions/validate-api-key.md) | `POST /validateApiKey` | [docs](https://documenter.getpostman.com/view/25361963/2s93Xzw2bS#d29ae242-4854-443e-8610-ee1403ab793b) |
