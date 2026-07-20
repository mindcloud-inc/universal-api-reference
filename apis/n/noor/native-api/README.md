# Noor: Native API Reference

A consolidated summary of Noor's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://usenoor.notion.site/Noor-Docs-48ff40fb312547a0aedfd5c0450d7a59
- **API base URL:** `https://sun.noor.to/api/v0`

## Authentication

### API Key

Use a Noor personal API key and Space ID.

### Credentials

- **API Key:** `apiKey` · required
- **Space ID:** `spaceId` · required · Your Noor Space ID from Settings > API.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.noor.to/preferences/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `members`.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Space Members](actions/list-space-members.md) | `POST /getSpaceMembers` | [docs](https://usenoor.notion.site/v0-e812ae5e5976420f81232fa1c0316e84) |
| [Send Message](actions/send-message.md) | `POST /sendMessage` | [docs](https://usenoor.notion.site/v0-e812ae5e5976420f81232fa1c0316e84) |
