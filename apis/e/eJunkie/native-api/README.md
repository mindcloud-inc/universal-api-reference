# E-junkie: Native API Reference

A consolidated summary of E-junkie's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.e-junkie.com/wiki/help-products-api
- **API base URL:** `https://api.e-junkie.com/api`

## Authentication

### API Key

Connect with your E-junkie seller Client ID and API key from the Products API page in Seller Admin. If the Products API menu is missing, enable the newer Admin interface via Try New Features first.

### Credentials

- **API Key:** `apiKey` · required
- **Client ID:** `clientId` · required · Your E-junkie seller Client ID from the Products API page in Seller Admin.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.e-junkie.com/wiki/help-products-api)

## API conventions

The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Products](actions/list-products.md) | `POST /{{credentials.clientId}}/` | [docs](https://www.e-junkie.com/wiki/help-products-api) |
