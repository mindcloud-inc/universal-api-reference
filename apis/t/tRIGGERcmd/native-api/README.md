# TRIGGERcmd: Native API Reference

A consolidated summary of TRIGGERcmd's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.triggercmd.com/
- **API base URL:** `https://www.triggercmd.com/api`

## Authentication

### API Token

Use the bearer token from the TRIGGERcmd Instructions page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.triggercmd.com/user/computer/create)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Commands](actions/list-commands.md) | `POST /command/list` | [docs](https://docs.triggercmd.com/#/API/ListCommands) |
| [Trigger Command](actions/trigger-command.md) | `POST /run/trigger` | [docs](https://docs.triggercmd.com/#/API/TriggerCommand) |
