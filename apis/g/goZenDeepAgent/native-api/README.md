# GoZen DeepAgent: Native API Reference

A consolidated summary of GoZen DeepAgent's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.gozen.io/deepagent/api-docs
- **API base URL:** `https://api.deepbot.gozen.io`

## Authentication

### API Key

Authenticate with a DeepAgent API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.gozen.io/deepagent/api-docs/zapier/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | `GET /integration/zapierapp/auth` | [docs](https://docs.gozen.io/deepagent/api-docs/zapier/get-profile) |
| [Register Webhook](actions/register-webhook.md) | `POST /integration/zapierapp/webhook` | [docs](https://docs.gozen.io/deepagent/api-docs/zapier/register-webhook) |
| [Unregister Webhook](actions/unregister-webhook.md) | `DELETE /integration/zapierapp/webhook` | [docs](https://docs.gozen.io/deepagent/api-docs/zapier/unregister-webhook) |
