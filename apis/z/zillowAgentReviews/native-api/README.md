# Zillow Agent Reviews: Native API Reference

A consolidated summary of Zillow Agent Reviews's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://bridgedataoutput.com/docs/platform
- **API base URL:** `https://api.bridgedataoutput.com/api/v2`

## Authentication

### Bridge server token

Bridge server token used as the access_token value for Bridge-hosted Zillow Agent Reviews requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bridgedataoutput.com/docs/platform)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List reviewees](actions/list-reviewees.md) | `GET /OData/reviews/Reviewees` | [docs](https://www.zillowgroup.com/developers/api/agents/agent-reviews/) |
| [List reviews](actions/list-reviews.md) | `GET /OData/reviews/Reviews` | [docs](https://www.zillowgroup.com/developers/api/agents/agent-reviews/) |
