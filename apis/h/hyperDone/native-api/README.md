# HyperDone: Native API Reference

A consolidated summary of HyperDone's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://help.hyperdone.com/public-api/
- **API base URL:** `https://hyperdone.com/api/public`

## Authentication

### Board API Key

Use a board-specific HyperDone API key from Board Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ApiKey: <apiKey>
```

[Official authentication documentation](https://help.hyperdone.com/public-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | `POST /AddTask` | [docs](https://help.hyperdone.com/public-api/) |
| [Get Board Info](actions/get-board-info.md) | `GET /GetBoardInfo` | [docs](https://help.hyperdone.com/public-api/) |
| [List Board Members](actions/list-board-members.md) | `GET /GetBoardMembers` | [docs](https://help.hyperdone.com/public-api/) |
| [List Columns](actions/list-columns.md) | `GET /GetColumns` | [docs](https://help.hyperdone.com/public-api/) |
| [List Tags](actions/list-tags.md) | `GET /GetTags` | [docs](https://help.hyperdone.com/public-api/) |
