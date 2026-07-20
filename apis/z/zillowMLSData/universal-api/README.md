# <img src="https://images.mindcloud.co/apps/icons/zillow-mlsdata_1776963742301.png" alt="Zillow MLS Data logo" width="28" height="28"> Zillow MLS Data: Universal API

Bridge-hosted Zillow MLS and OData data access. Requires a Bridge account and approved datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zillowMLSData/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/
- **Vendor API docs:** https://bridgedataoutput.com/docs/platform

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List datasets](actions/list-datasets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-datasets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get data systems](actions/get-data-systems.md) | GET | Retrieves data systems from Zillow MLS Data. |
| [List datasets](actions/list-datasets.md) | GET | Retrieves available datasets from Zillow MLS Data. |

### Offices

| Action | Method | Description |
| --- | --- | --- |
| [Get office](actions/get-office.md) | GET | Retrieves a specific office from Zillow MLS Data. |
| [Get office (OData)](actions/get-office-o-data.md) | GET | Retrieves an office record from Zillow MLS Data using OData. |
| [List offices](actions/list-offices.md) | GET | Retrieves offices from a Zillow MLS Data dataset. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get listing](actions/get-listing.md) | GET | Retrieves a specific listing from Zillow MLS Data. |
| [Get property (OData)](actions/get-property-o-data.md) | GET | Retrieves a property record from Zillow MLS Data using OData. |
| [List IDX field rules (OData)](actions/list-idx-field-rules-o-data.md) | GET | Retrieves IDX field rules from Zillow MLS Data using OData. |
| [List IDX properties (OData)](actions/list-idx-properties-o-data.md) | GET | Retrieves IDX property records from Zillow MLS Data using OData. |
| [List listings](actions/list-listings.md) | GET | Retrieves listings from a Zillow MLS Data dataset. |
| [List properties (OData)](actions/list-properties-o-data.md) | GET | Retrieves property records from Zillow MLS Data using OData. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get agent](actions/get-agent.md) | GET | Retrieves a specific agent from Zillow MLS Data. |
| [Get member (OData)](actions/get-member-o-data.md) | GET | Retrieves a member record from Zillow MLS Data using OData. |
| [List agents](actions/list-agents.md) | GET | Retrieves agents from a Zillow MLS Data dataset. |

