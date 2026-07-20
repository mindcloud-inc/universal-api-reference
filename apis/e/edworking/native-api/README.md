# Edworking: Native API Reference

A consolidated summary of Edworking's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://edworking.com/api/overview/get-started
- **API base URL:** `https://gateway.edworking.com`

## Authentication

### API Key

Use a personal Edworking API token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://edworking.com/api/overview/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | `POST /` | [docs](https://edworking.com/api/queries/getNotifications) |
