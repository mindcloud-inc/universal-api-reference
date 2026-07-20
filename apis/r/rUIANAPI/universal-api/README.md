# <img src="https://images.mindcloud.co/apps/icons/r-uianapi_1776094463027.png" alt="RUIAN logo" width="28" height="28"> RUIAN: Universal API

Browse and export RÚIAN public registry data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rUIANAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ruian.cuzk.cz/
- **Vendor API docs:** https://developers.arcgis.com/rest/services-reference/enterprise/map-service/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all layers and tables](actions/get-all-layers-and-tables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/get-all-layers-and-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Get all layers and tables](actions/get-all-layers-and-tables.md) | GET | Retrieves layers and tables from RUIAN API. |
| [Get layer details](actions/get-layer-details.md) | GET | Retrieves layer details from RUIAN API. |
| [Get service details](actions/get-service-details.md) | GET | Retrieves service details from RUIAN API. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Query layer features](actions/query-layer-features.md) | GET | Retrieves layer features from RUIAN API. |

