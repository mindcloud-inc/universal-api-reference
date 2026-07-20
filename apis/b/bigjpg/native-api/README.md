# Bigjpg: Native API Reference

A consolidated summary of Bigjpg's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://bigjpg.com/
- **API base URL:** `https://bigjpg.com/api`

## Authentication

### API Key

Connect Bigjpg using the provider-native API key from the authenticated Bigjpg API tab.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://bigjpg.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Enlarge Task](actions/create-enlarge-task.md) | `POST /task/` | [docs](https://bigjpg.com/) |
| [Get Task Result](actions/get-task-result.md) | `GET /task/:taskIds` | [docs](https://bigjpg.com/) |
| [Retry Task](actions/retry-task.md) | `POST /task/:taskIds` | [docs](https://bigjpg.com/) |
