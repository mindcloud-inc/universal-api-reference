# <img src="https://images.mindcloud.co/apps/icons/favicon-openbrewerydb-org-48x48_1777643279184.png" alt="Open Brewery DB logo" width="28" height="28"> Open Brewery DB: Universal API

Open Brewery DB is a free public dataset and REST API for brewery, cidery, brewpub, and bottleshop information.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openBreweryDB/latest
- **Category:** IT Operations / Database
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openbrewerydb.org/
- **Vendor API docs:** https://openbrewerydb.org/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Breweries](actions/list-breweries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/list-breweries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Brewery

| Action | Method | Description |
| --- | --- | --- |
| [Get Brewery](actions/get-brewery.md) | GET | Retrieves a brewery from Open Brewery DB. |
| [List Breweries](actions/list-breweries.md) | GET | Retrieves breweries from Open Brewery DB. |
| [List Random Breweries](actions/list-random-breweries.md) | GET | Retrieves random breweries from Open Brewery DB. |
| [Search Breweries](actions/search-breweries.md) | GET | Finds breweries in Open Brewery DB by search term. |

### Brewery Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Brewery Metadata](actions/get-brewery-metadata.md) | GET | Retrieves brewery metadata from Open Brewery DB. |

