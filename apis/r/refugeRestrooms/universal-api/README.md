# <img src="https://images.mindcloud.co/apps/icons/refuge-restrooms_1777487325242.png" alt="Refuge Restrooms logo" width="28" height="28"> Refuge Restrooms: Universal API

Official open-source restroom finder for safe, accessible, and unisex restroom records from Refuge Restrooms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/refugeRestrooms/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.refugerestrooms.org
- **Vendor API docs:** https://www.refugerestrooms.org/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Restrooms](actions/list-restrooms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/list-restrooms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Restroom

| Action | Method | Description |
| --- | --- | --- |
| [List Restrooms](actions/list-restrooms.md) | GET |  |
| [Search Restrooms](actions/search-restrooms.md) | GET |  |
| [Search Restrooms by Date](actions/search-restrooms-by-date.md) | GET |  |
| [Search Restrooms by Location](actions/search-restrooms-by-location.md) | GET |  |

