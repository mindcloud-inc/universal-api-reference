# Verify (Tailr Made): Native API Reference

A consolidated summary of Verify (Tailr Made)'s API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://tailrmadeai.com/developer-dashboard/
- **API base URL:** `https://api.tailrmadeai.com`

## Authentication

### API Key

Tailr Made API key authentication

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://tailrmadeai.com/developer-dashboard/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Verify Resume Red Flags](actions/verify-resume-red-flags.md) | `POST /api/verify` | [docs](https://tailrmadeai.com/verify-api-guide/) |
