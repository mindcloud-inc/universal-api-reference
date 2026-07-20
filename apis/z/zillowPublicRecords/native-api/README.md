# Zillow Public Records: Native API Reference

A consolidated summary of Zillow Public Records's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://bridgedataoutput.com/docs/platform
- **API base URL:** `https://api.bridgedataoutput.com/api/v2`

## Authentication

### Bridge server token

Bridge server token used as the access_token value for Bridge-hosted Zillow Public Records requests.

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
| [List assessments](actions/list-assessments.md) | `GET /pub/assessments` | [docs](https://www.zillowgroup.com/developers/api/public-data/public-records-api/) |
| [List parcel transactions](actions/list-parcel-transactions.md) | `GET /pub/parcels/:parcelId/transactions` | [docs](https://www.zillowgroup.com/developers/api/public-data/public-records-api/) |
