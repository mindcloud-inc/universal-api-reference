# Promptmate.io: Native API Reference

A consolidated summary of Promptmate.io's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://apidoc.promptmate.io/
- **API base URL:** `https://api.promptmate.io/v1`

## Authentication

### API Key

Use your Promptmate.io API key. Promptmate requires the key in the x-api-key header and does not use bearer Authorization for this API.

### Credentials

- **API Key:** `apiKey` · required · Your Promptmate.io API key. Promptmate requires this value in the x-api-key request header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://apidoc.promptmate.io/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `promptmate.io` |

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create App Job](actions/create-app-job.md) | `POST /app-jobs` | [docs](https://apidoc.promptmate.io/api-4935445) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://apidoc.promptmate.io/api-5407074) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks` | [docs](https://apidoc.promptmate.io/api-5407075) |
| [Get App Result Rows](actions/get-app-result-rows.md) | `GET /app-results` | [docs](https://apidoc.promptmate.io/api-5431941) |
| [Get User Information](actions/get-user-information.md) | `GET /userInfo` | [docs](https://apidoc.promptmate.io/api-5460353) |
| [List Apps](actions/list-apps.md) | `GET /apps` | [docs](https://apidoc.promptmate.io/) |
| [List Countries](actions/list-countries.md) | `GET /reference/countries` | [docs](https://apidoc.promptmate.io/api-5087001) |
| [List Languages](actions/list-languages.md) | `GET /reference/languages` | [docs](https://apidoc.promptmate.io/api-5087000) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://apidoc.promptmate.io/api-5089195) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://apidoc.promptmate.io/api-4935447) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://apidoc.promptmate.io/api-5407073) |
| [Use Template](actions/use-template.md) | `POST /templates/use` | [docs](https://apidoc.promptmate.io/api-4935448) |
