# MENU TIGER: Native API Reference

A consolidated summary of MENU TIGER's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://menutiger.helpscoutdocs.com/article/41-how-to-integrate-zapier-to-menu-tiger
- **API base URL:** `https://alb.menutigr.com/api`

## Authentication

### API Key

Authenticate MENU TIGER Zapier endpoints with a MENU TIGER developer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://menutiger.helpscoutdocs.com/article/41-how-to-integrate-zapier-to-menu-tiger)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Integration Status](actions/get-integration-status.md) | `GET /zapier/status` | [docs](https://menutiger.helpscoutdocs.com/article/41-how-to-integrate-zapier-to-menu-tiger) |
| [List Customers](actions/list-customers.md) | `GET /zapier/customers` | [docs](https://menutiger.helpscoutdocs.com/article/41-how-to-integrate-zapier-to-menu-tiger) |
| [List Orders](actions/list-orders.md) | `GET /zapier/orders` | [docs](https://menutiger.helpscoutdocs.com/article/41-how-to-integrate-zapier-to-menu-tiger) |
