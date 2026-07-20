# <img src="https://images.mindcloud.co/apps/icons/bridge-interactive-platform_1776947664597.png" alt="Bridge Interactive Platform logo" width="28" height="28"> Bridge Interactive Platform: Universal API

Access Bridge Interactive listing data through the Bridge Web API and RESO Web API. This app covers the officially documented read surfaces for listings, agents, offices, open houses, members, properties, and lookup metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bridgeInteractivePlatform/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bridgedataoutput.com/
- **Vendor API docs:** https://bridgedataoutput.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-agents?connectionId=$CONNECTION_ID&dataset=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get open house](actions/get-open-house.md) | GET | Retrieves an open house from Bridge Interactive Platform. |
| [Get open house (OData)](actions/get-open-house-o-data.md) | GET | Retrieves an open house from Bridge Interactive Platform. |
| [List open houses](actions/list-open-houses.md) | GET | Retrieves open house records from Bridge Interactive Platform. |
| [List open houses (OData)](actions/list-open-houses-o-data.md) | GET | Retrieves open house records from Bridge Interactive Platform. |

### Offices

| Action | Method | Description |
| --- | --- | --- |
| [Get office](actions/get-office.md) | GET | Retrieves an office from Bridge Interactive Platform. |
| [Get office (OData)](actions/get-office-o-data.md) | GET | Retrieves an office from Bridge Interactive Platform. |
| [List offices](actions/list-offices.md) | GET | Retrieves office records from Bridge Interactive Platform. |
| [List offices (OData)](actions/list-offices-o-data.md) | GET | Retrieves office records from Bridge Interactive Platform. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get listing](actions/get-listing.md) | GET | Retrieves a listing from Bridge Interactive Platform. |
| [Get property (OData)](actions/get-property-o-data.md) | GET | Retrieves a property from Bridge Interactive Platform. |
| [List listings](actions/list-listings.md) | GET | Retrieves listing records from Bridge Interactive Platform. |
| [List lookups (OData)](actions/list-lookups-o-data.md) | GET | Retrieves lookup records from Bridge Interactive Platform. |
| [List properties (OData)](actions/list-properties-o-data.md) | GET | Retrieves property records from Bridge Interactive Platform. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get agent](actions/get-agent.md) | GET | Retrieves an agent from Bridge Interactive Platform. |
| [Get member (OData)](actions/get-member-o-data.md) | GET | Retrieves a member from Bridge Interactive Platform. |
| [List agents](actions/list-agents.md) | GET | Retrieves agent records from Bridge Interactive Platform. |
| [List members (OData)](actions/list-members-o-data.md) | GET | Retrieves member records from Bridge Interactive Platform. |

