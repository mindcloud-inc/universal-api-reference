# <img src="https://images.mindcloud.co/apps/icons/rick-and-morty_1785420669825.png" alt="Rick and Morty logo" width="28" height="28"> Rick and Morty: Universal API

Public read-only wrapper for The Rick and Morty API, exposing characters, locations, and episodes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rickAndMorty/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rickandmortyapi.com/
- **Vendor API docs:** https://rickandmortyapi.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Character](actions/get-character.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

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

