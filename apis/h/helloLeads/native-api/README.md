# HelloLeads: Native API Reference

A consolidated summary of HelloLeads's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://app.helloleads.io/index.php/app/account/layout#/apisettings
- **API base URL:** `https://app.helloleads.io/index.php/private/api`

## Authentication

### API Key

Authenticate HelloLeads requests with the account API key and the authorized email tied to that key.

### Credentials

- **API Key:** `apiKey` · required
- **Authorized Email:** `email` · required · The authorized HelloLeads account email paired with this API key. HelloLeads sends this value in the Xemail header at runtime.

Send these headers with each API request:

```http
Xemail: <email>
```

[Official authentication documentation](https://app.helloleads.io/index.php/app/account/layout#/apisettings)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The total page count is read from `paging.total_pages`. The current page number is read from `paging.current_page`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | `POST leads` | [docs](https://app.helloleads.io/index.php/app/account/layout#/apisettings) |
| [List Lead Lists](actions/list-lead-lists.md) | `GET lists` | [docs](https://app.helloleads.io/index.php/app/account/layout#/apisettings) |
| [List Leads](actions/list-leads.md) | `GET leadsOrderBy` | [docs](https://app.helloleads.io/index.php/app/account/layout#/apisettings) |
