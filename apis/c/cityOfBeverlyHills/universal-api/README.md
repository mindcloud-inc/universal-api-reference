# <img src="https://images.mindcloud.co/apps/icons/city-of-beverly-hills_1776374848789.png" alt="City of Beverly Hills logo" width="28" height="28"> City of Beverly Hills: Universal API

Public ArcGIS open data portal for the City of Beverly Hills.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cityOfBeverlyHills/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services/
- **Vendor API docs:** https://opendata-hub.beverlyhills.org/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Layer](actions/get-feature-layer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-layer?connectionId=$CONNECTION_ID&layerId=string&serviceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Layer](actions/get-feature-layer.md) | GET | Retrieves feature layer details from City of Beverly Hills. |
| [Get Feature Service](actions/get-feature-service.md) | GET | Retrieves feature service details from City of Beverly Hills. |
| [List Services](actions/list-services.md) | GET | Retrieves ArcGIS service records from City of Beverly Hills. |
| [Query Features](actions/query-features.md) | GET | Queries layer features in City of Beverly Hills by service and layer. |

