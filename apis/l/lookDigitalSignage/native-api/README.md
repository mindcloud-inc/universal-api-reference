# Look Digital Signage: Native API Reference

A consolidated summary of Look Digital Signage's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.lookdigitalsignage.com/knowledge-base/actions
- **API base URL:** `https://api.lookit.hk/api/v1/external/actions`

## Authentication

### Action API Key

Authenticate Look Digital Signage actions with the Look Action API key from Company Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
look-api-key: <apiKey>
```

[Official authentication documentation](https://www.lookdigitalsignage.com/knowledge-base/create-action-trigger)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Trigger Action](actions/trigger-action.md) | `GET https://api.lookit.hk/api/v1/external/actions/:actionLink` | [docs](https://www.lookdigitalsignage.com/knowledge-base/create-action-trigger) |
