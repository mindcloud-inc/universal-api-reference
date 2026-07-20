# <img src="https://images.mindcloud.co/apps/icons/body-graph_1773839793798.png" alt="BodyGraph logo" width="28" height="28"> BodyGraph: Universal API

Generate Human Design and astrology chart data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bodyGraph/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bodygraph.com
- **Vendor API docs:** https://bodygraph.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Locations](actions/search-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/search-locations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Astrology Chart

| Action | Method | Description |
| --- | --- | --- |
| [Generate Astrology Data](actions/generate-astrology-data.md) | GET | Retrieves astrology chart data from BodyGraph. |

### Human Design Chart

| Action | Method | Description |
| --- | --- | --- |
| [Generate HD Data](actions/generate-hd-data.md) | GET | Retrieves Human Design chart data from BodyGraph. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Search Locations](actions/search-locations.md) | GET | Finds locations in BodyGraph by search term. |

