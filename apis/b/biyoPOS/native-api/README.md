# Biyo POS: Native API Reference

A consolidated summary of Biyo POS's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://biyopos.com/encyclopedia/api-application-programming-interface/
- **API base URL:** `https://mindcloud.biyo.co`

## Authentication

### API Key

Provider-generated API key authentication for Biyo POS.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://biyo.tawk.help/article/how-to-add-api-key)

## API conventions

Response data is read from `results`. The total page count is read from `max_pages`. The current page number is read from `current_page`.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | `GET /api/v1/categories/` | [docs](https://biyopos.com/encyclopedia/api-application-programming-interface/) |
| [List Customers](actions/list-customers.md) | `GET /api/v1/customers/` | [docs](https://biyopos.com/encyclopedia/api-application-programming-interface/) |
| [List Orders](actions/list-orders.md) | `GET /api/v1/orders/` | [docs](https://biyopos.com/encyclopedia/api-application-programming-interface/) |
| [List Products](actions/list-products.md) | `GET /api/v1/products/` | [docs](https://biyopos.com/encyclopedia/api-application-programming-interface/) |
