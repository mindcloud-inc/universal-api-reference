# Customer.guru: Native API Reference

A consolidated summary of Customer.guru's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://customer.guru/api/documentation/v2
- **API base URL:** `https://customer.guru`

## Authentication

### API Key

Use your Customer.guru API token and API secret.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · Customer.guru API secret.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://customer.guru/api/documentation/v2)

## Pagination

Use `per_page` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Customers](actions/export-customers.md) | `GET /export/customers` | [docs](https://customer.guru/api/documentation/v2#receiving) |
| [Export Ratings](actions/export-ratings.md) | `GET /export/ratings` | [docs](https://customer.guru/api/documentation/v2) |
| [Send Survey](actions/send-survey.md) | `POST /api/v2/survey` | [docs](https://customer.guru/api/documentation/v2) |
