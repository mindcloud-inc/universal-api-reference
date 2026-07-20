# Zillow Zestimates: Native API Reference

A consolidated summary of Zillow Zestimates's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://bridgedataoutput.com/docs/platform
- **API base URL:** `https://api.bridgedataoutput.com/api/v2`

## Authentication

### Bridge server token

Bridge server token used as the access_token value for Bridge-hosted Zillow Zestimate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bridgedataoutput.com/docs/platform)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List zestimates](actions/list-zestimates.md) | `GET /zestimates_v2/zestimates` | [docs](https://www.zillowgroup.com/developers/api/zestimate/zestimates-api/) |
