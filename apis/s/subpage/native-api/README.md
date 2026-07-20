# Subpage: Native API Reference

A consolidated summary of Subpage's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://helpcenter.subpage.app/article/zapier-api-integration
- **API base URL:** `https://editor.subpage.app`

## Authentication

### API Key

Use a Subpage integrations token from the Integrations page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://helpcenter.subpage.app/article/how-to-enable-zapier-integration)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | `GET /call/api/zapier/validateuser` | [docs](https://helpcenter.subpage.app/article/zapier-api-integration) |
| [List New Articles](actions/list-new-articles.md) | `GET /call/api/zapier/listtrigger` | [docs](https://helpcenter.subpage.app/article/zapier-api-integration) |
| [List New Leads](actions/list-new-leads.md) | `GET /call/api/zapier/listtrigger` | [docs](https://helpcenter.subpage.app/article/zapier-api-integration) |
| [List Trigger Notifications](actions/list-trigger-notifications.md) | `GET /call/api/zapier/listtrigger` | [docs](https://helpcenter.subpage.app/article/zapier-api-integration) |
