# SalesRender: Native API Reference

A consolidated summary of SalesRender's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://wiki.salesrender.com/en/home/plugin/api
- **API base URL:** `https://de.backend.salesrender.com/companies`

## Authentication

### API Token

Authenticate with a SalesRender API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://wiki.salesrender.com/en/home/plugin/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | SalesRender company ID from your own account UI. This must match the company that issued the API token used by the connection. |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [Create Order](actions/create-order.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [Create User](actions/create-user.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [Get Company](actions/get-company.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Customers](actions/list-customers.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Item Categories](actions/list-item-categories.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Items](actions/list-items.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Offers](actions/list-offers.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Orders](actions/list-orders.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Projects](actions/list-projects.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Roles](actions/list-roles.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Statuses](actions/list-statuses.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Targets](actions/list-targets.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Users](actions/list-users.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [List Warehouses](actions/list-warehouses.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [Update Item](actions/update-item.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [Update Order](actions/update-order.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
| [Update User](actions/update-user.md) | `POST :companyId/CRM` | [docs](https://wiki.salesrender.com/en/home/plugin/api) |
