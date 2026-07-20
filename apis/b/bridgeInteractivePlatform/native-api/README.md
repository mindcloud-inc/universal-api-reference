# Bridge Interactive Platform: Native API Reference

A consolidated summary of Bridge Interactive Platform's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://bridgedataoutput.com/docs
- **OpenAPI specification:** https://bridgedataoutput.com/tuberat/swagger
- **API base URL:** `https://api.bridgedataoutput.com/api/v2`

## Authentication

### Server token

Bridge server token used as the access_token query parameter for Bridge Web API and RESO Web API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bridgedataoutput.com/docs)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This run validated the tenant against dataset test. |

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get agent](actions/get-agent.md) | `GET /:dataset/agents/:agentId` | [docs](https://bridgedataoutput.com/docs) |
| [Get listing](actions/get-listing.md) | `GET /:dataset/listings/:listingId` | [docs](https://bridgedataoutput.com/docs) |
| [Get member (OData)](actions/get-member-o-data.md) | `GET /OData/:dataset/Member(':MemberKey')` | [docs](https://bridgedataoutput.com/docs) |
| [Get office](actions/get-office.md) | `GET /:dataset/offices/:officeId` | [docs](https://bridgedataoutput.com/docs) |
| [Get office (OData)](actions/get-office-o-data.md) | `GET /OData/:dataset/Office(':OfficeKey')` | [docs](https://bridgedataoutput.com/docs) |
| [Get open house](actions/get-open-house.md) | `GET /:dataset/openhouses/:openhouseId` | [docs](https://bridgedataoutput.com/docs) |
| [Get open house (OData)](actions/get-open-house-o-data.md) | `GET /OData/:dataset/OpenHouse(':OpenHouseKey')` | [docs](https://bridgedataoutput.com/docs) |
| [Get property (OData)](actions/get-property-o-data.md) | `GET /OData/:dataset/Property(':ListingKey')` | [docs](https://bridgedataoutput.com/docs) |
| [List agents](actions/list-agents.md) | `GET /:dataset/agents` | [docs](https://bridgedataoutput.com/docs) |
| [List listings](actions/list-listings.md) | `GET /:dataset/listings` | [docs](https://bridgedataoutput.com/docs) |
| [List lookups (OData)](actions/list-lookups-o-data.md) | `GET /OData/:dataset/Lookup` | [docs](https://bridgedataoutput.com/docs) |
| [List members (OData)](actions/list-members-o-data.md) | `GET /OData/:dataset/Member` | [docs](https://bridgedataoutput.com/docs) |
| [List offices](actions/list-offices.md) | `GET /:dataset/offices` | [docs](https://bridgedataoutput.com/docs) |
| [List offices (OData)](actions/list-offices-o-data.md) | `GET /OData/:dataset/Office` | [docs](https://bridgedataoutput.com/docs) |
| [List open houses](actions/list-open-houses.md) | `GET /:dataset/openhouses` | [docs](https://bridgedataoutput.com/docs) |
| [List open houses (OData)](actions/list-open-houses-o-data.md) | `GET /OData/:dataset/OpenHouse` | [docs](https://bridgedataoutput.com/docs) |
| [List properties (OData)](actions/list-properties-o-data.md) | `GET /OData/:dataset/Property` | [docs](https://bridgedataoutput.com/docs) |
