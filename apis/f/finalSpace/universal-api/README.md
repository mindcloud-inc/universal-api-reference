# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423471289.png" alt="Final Space logo" width="28" height="28"> Final Space: Universal API

Final Space through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finalSpace/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Character](actions/get-character.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | GET |  |
| [List Characters](actions/list-characters.md) | GET |  |

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode](actions/get-episode.md) | GET |  |
| [List Episodes](actions/list-episodes.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [List Quotes](actions/list-quotes.md) | GET |  |

