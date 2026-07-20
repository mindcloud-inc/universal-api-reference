# Zillow MLS Data: Native API Reference

A consolidated summary of Zillow MLS Data's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://bridgedataoutput.com/docs/platform
- **API base URL:** `https://api.bridgedataoutput.com/api/v2`

## Authentication

### Bridge server token

Bridge server token used as the access_token value for Bridge-hosted Zillow MLS data requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bridgedataoutput.com/docs/platform)

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get agent](actions/get-agent.md) | `GET /:dataset/agents/:agentId` | [docs](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/) |
| [Get data systems](actions/get-data-systems.md) | `GET /OData/DataSystem` | [docs](https://bridgedataoutput.com/docs/platform) |
| [Get listing](actions/get-listing.md) | `GET /:dataset/listings/:listingId` | [docs](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/) |
| [Get member (OData)](actions/get-member-o-data.md) | `GET /OData/:dataset/Members(':memberKey')` | [docs](https://bridgedataoutput.com/docs/platform) |
| [Get office](actions/get-office.md) | `GET /:dataset/offices/:officeId` | [docs](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/) |
| [Get office (OData)](actions/get-office-o-data.md) | `GET /OData/:dataset/Offices(':officeKey')` | [docs](https://bridgedataoutput.com/docs/platform) |
| [Get property (OData)](actions/get-property-o-data.md) | `GET /OData/:dataset/Properties(':listingKey')` | [docs](https://bridgedataoutput.com/docs/platform) |
| [List agents](actions/list-agents.md) | `GET /:dataset/agents` | [docs](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/) |
| [List datasets](actions/list-datasets.md) | `GET /datasets` | [docs](https://bridgedataoutput.com/docs/platform) |
| [List IDX field rules (OData)](actions/list-idx-field-rules-o-data.md) | `GET /OData/:dataset/idx/Field` | [docs](https://bridgedataoutput.com/docs/platform) |
| [List IDX properties (OData)](actions/list-idx-properties-o-data.md) | `GET /OData/:dataset/idx/Properties` | [docs](https://bridgedataoutput.com/docs/platform) |
| [List listings](actions/list-listings.md) | `GET /:dataset/listings` | [docs](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/) |
| [List offices](actions/list-offices.md) | `GET /:dataset/offices` | [docs](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/) |
| [List properties (OData)](actions/list-properties-o-data.md) | `GET /OData/:dataset/Properties` | [docs](https://bridgedataoutput.com/docs/platform) |
