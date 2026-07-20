# vionvi CRM: Native API Reference

A consolidated summary of vionvi CRM's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://280-crm-api.vionvi.com/
- **API base URL:** `https://280-crm-api.vionvi.com`

## Authentication

### API key

Bearer token authentication for the tenant-scoped vionvi CRM API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://280-crm-api.vionvi.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Clients](actions/count-clients.md) | `GET /client/count` | [docs](https://280-crm-api.vionvi.com/) |
| [Count Contracts](actions/count-contracts.md) | `GET /contract/count` | [docs](https://280-crm-api.vionvi.com/) |
| [Count Leads](actions/count-leads.md) | `GET /lead/count` | [docs](https://280-crm-api.vionvi.com/) |
| [Count Payments](actions/count-payments.md) | `GET /pay/count` | [docs](https://280-crm-api.vionvi.com/) |
| [Count Tasks](actions/count-tasks.md) | `GET /task/count` | [docs](https://280-crm-api.vionvi.com/) |
| [Count Users](actions/count-users.md) | `GET /user/count` | [docs](https://280-crm-api.vionvi.com/) |
| [List Catalog Items](actions/list-catalog-items.md) | `GET /catalog` | [docs](https://280-crm-api.vionvi.com/) |
| [List Chats](actions/list-chats.md) | `GET /chat` | [docs](https://280-crm-api.vionvi.com/) |
| [List Clients](actions/list-clients.md) | `GET /client` | [docs](https://280-crm-api.vionvi.com/) |
| [List Contracts](actions/list-contracts.md) | `GET /contract` | [docs](https://280-crm-api.vionvi.com/) |
| [List Currencies](actions/list-currencies.md) | `GET /currency/all-list` | [docs](https://280-crm-api.vionvi.com/) |
| [List Funnels](actions/list-funnels.md) | `GET /funnel` | [docs](https://280-crm-api.vionvi.com/) |
| [List Leads](actions/list-leads.md) | `GET /lead` | [docs](https://280-crm-api.vionvi.com/) |
| [List Organizations](actions/list-organizations.md) | `GET /org` | [docs](https://280-crm-api.vionvi.com/) |
| [List Payments](actions/list-payments.md) | `GET /pay` | [docs](https://280-crm-api.vionvi.com/) |
| [List Permissions](actions/list-permissions.md) | `GET /permission` | [docs](https://280-crm-api.vionvi.com/) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://280-crm-api.vionvi.com/) |
| [List Roles](actions/list-roles.md) | `GET /role` | [docs](https://280-crm-api.vionvi.com/) |
| [List Services](actions/list-services.md) | `GET /service` | [docs](https://280-crm-api.vionvi.com/) |
| [List Sources](actions/list-sources.md) | `GET /source` | [docs](https://280-crm-api.vionvi.com/) |
| [List Task Statuses](actions/list-task-statuses.md) | `GET /task/status-list` | [docs](https://280-crm-api.vionvi.com/) |
| [List Tasks](actions/list-tasks.md) | `GET /task` | [docs](https://280-crm-api.vionvi.com/) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://280-crm-api.vionvi.com/) |
| [Show Current User](actions/show-current-user.md) | `GET /user/show-me` | [docs](https://280-crm-api.vionvi.com/) |
