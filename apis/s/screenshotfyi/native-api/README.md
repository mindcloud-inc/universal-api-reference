# screenshot.fyi: Native API Reference

A consolidated summary of screenshot.fyi's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.screenshot.fyi/
- **API base URL:** `https://screenshot.fyi/api`

## Authentication

### API Key

Use your screenshot.fyi access key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.screenshot.fyi/)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Take Screenshot](actions/take-screenshot.md) | `GET /take` | [docs](https://www.screenshot.fyi/) |
