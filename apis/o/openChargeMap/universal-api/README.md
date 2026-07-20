# <img src="https://images.mindcloud.co/apps/icons/open-charge-map_1777563262207.png" alt="Open Charge Map logo" width="28" height="28"> Open Charge Map: Universal API

Find and inspect electric vehicle charging location data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openChargeMap/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openchargemap.org
- **Vendor API docs:** https://www.openchargemap.org/develop/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Core Reference Data](actions/get-core-reference-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-core-reference-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Charging Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Charging Location By ID](actions/get-charging-location-by-id.md) | GET |  |
| [List Charging Locations Along Route](actions/list-charging-locations-along-route.md) | GET |  |
| [List Charging Locations By Country Code](actions/list-charging-locations-by-country-code.md) | GET |  |
| [List Charging Locations By Country ID](actions/list-charging-locations-by-country-id.md) | GET |  |
| [List Charging Locations In Bounding Box](actions/list-charging-locations-in-bounding-box.md) | GET |  |
| [List Charging Locations In Polygon](actions/list-charging-locations-in-polygon.md) | GET |  |
| [List Locations After ID](actions/list-locations-after-id.md) | GET |  |
| [List Locations By Connection Type](actions/list-locations-by-connection-type.md) | GET |  |
| [List Locations By Data Provider](actions/list-locations-by-data-provider.md) | GET |  |
| [List Locations By Operator](actions/list-locations-by-operator.md) | GET |  |
| [List Locations By Status Type](actions/list-locations-by-status-type.md) | GET |  |
| [List Locations By Usage Type](actions/list-locations-by-usage-type.md) | GET |  |
| [List Locations With Comments](actions/list-locations-with-comments.md) | GET |  |
| [List Nearby Charging Locations](actions/list-nearby-charging-locations.md) | GET |  |
| [List Open Data Locations](actions/list-open-data-locations.md) | GET |  |
| [List Recently Modified Locations](actions/list-recently-modified-locations.md) | GET |  |
| [Search Charging Locations](actions/search-charging-locations.md) | GET |  |

### Openapi Definition

| Action | Method | Description |
| --- | --- | --- |
| [Get OpenAPI Definition](actions/get-open-api-definition.md) | GET |  |

### Reference Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Core Reference Data](actions/get-core-reference-data.md) | GET |  |
| [Get Reference Data By Country ID](actions/get-reference-data-by-country-id.md) | GET |  |

