# Doppler Farhan Latif: Native API Reference

A consolidated summary of Doppler Farhan Latif's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.doppler.com/reference/api
- **API base URL:** `https://api.doppler.com`

## Authentication

### Developer API Key

Authenticate with a Doppler developer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.doppler.com/reference/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `projects`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Secret](actions/delete-secret.md) | `DELETE /v3/configs/config/secret` | [docs](https://docs.doppler.com/reference/secrets-delete) |
| [Get Config](actions/get-config.md) | `GET /v3/configs/config` | [docs](https://docs.doppler.com/reference/configs-get) |
| [Get Config Log](actions/get-config-log.md) | `GET /v3/configs/config/logs/log` | [docs](https://docs.doppler.com/reference/config_logs-get) |
| [Get Project](actions/get-project.md) | `GET /v3/projects/project` | [docs](https://docs.doppler.com/reference/projects-get) |
| [Get Secret](actions/get-secret.md) | `GET /v3/configs/config/secret` | [docs](https://docs.doppler.com/reference/secrets-get) |
| [List Config Logs](actions/list-config-logs.md) | `GET /v3/configs/config/logs` | [docs](https://docs.doppler.com/reference/config_logs-list) |
| [List Configs](actions/list-configs.md) | `GET /v3/configs` | [docs](https://docs.doppler.com/reference/configs-list) |
| [List Environments](actions/list-environments.md) | `GET /v3/environments` | [docs](https://docs.doppler.com/reference/environments-list) |
| [List Projects](actions/list-projects.md) | `GET /v3/projects` | [docs](https://docs.doppler.com/reference/projects-list) |
| [List Secret Names](actions/list-secret-names.md) | `GET /v3/configs/config/secrets/names` | [docs](https://docs.doppler.com/reference/secrets-names) |
| [List Secrets](actions/list-secrets.md) | `GET /v3/configs/config/secrets` | [docs](https://docs.doppler.com/reference/secrets-list) |
| [Update Secret Note](actions/update-secret-note.md) | `POST /v3/projects/project/note` | [docs](https://docs.doppler.com/reference/secrets-update_note) |
| [Update Secrets](actions/update-secrets.md) | `POST /v3/configs/config/secrets` | [docs](https://docs.doppler.com/reference/secrets-update) |
