# <img src="https://images.mindcloud.co/apps/icons/melo_1775249934325.png" alt="Melo logo" width="28" height="28"> Melo: Universal API

Melo provides real-estate data APIs for querying property listings, indicators, locations, saved searches, and webhook-driven events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/melo/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.melo.io/status/
- **Vendor API docs:** https://docs.melo.io/api-reference/concepts

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Departments](actions/list-departments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### City

| Action | Method | Description |
| --- | --- | --- |
| [List Cities](actions/list-cities.md) | GET | Retrieves cities from Melo matching the provided criteria. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Search Locations](actions/search-locations.md) | GET | Finds locations in Melo by search term. |

### Point Of Interest

| Action | Method | Description |
| --- | --- | --- |
| [List Points of Interest](actions/list-points-of-interest.md) | GET | Retrieves points of interest from Melo near specific coordinates. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Create Search](actions/create-search.md) | POST | Creates a new search in Melo. |
| [Delete Search](actions/delete-search.md) | DELETE | Deletes an existing search from Melo. |
| [Get Search](actions/get-search.md) | GET | Retrieves details for an existing search from Melo. |
| [List Searches](actions/list-searches.md) | GET | Retrieves existing searches from Melo matching the current criteria. |
| [Update Search](actions/update-search.md) | PUT | Updates an existing search in Melo. |

