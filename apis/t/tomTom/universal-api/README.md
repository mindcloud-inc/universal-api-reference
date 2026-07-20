# <img src="https://images.mindcloud.co/apps/icons/tomtom-icon-square-1024_1776351728782.png" alt="TomTom logo" width="28" height="28"> TomTom: Universal API

TomTom provides mapping, routing, search, traffic, geocoding, geofencing, matrix, and related location intelligence APIs for building location-aware applications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tomTom/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tomtom.com/
- **Vendor API docs:** https://developer.tomtom.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List POI Categories](actions/list-poi-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomTom/latest/actions/list-poi-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List POI Categories](actions/list-poi-categories.md) | GET | Retrieves available POI categories from TomTom. |

