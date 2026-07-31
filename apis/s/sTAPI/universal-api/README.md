# <img src="https://images.mindcloud.co/apps/icons/s-tapi_1785363431221.png" alt="STAPI logo" width="28" height="28"> STAPI: Universal API

Explore Star Trek characters, episodes, places, spacecraft, and media

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sTAPI/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stapi.co
- **Vendor API docs:** https://stapi.co/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Character](actions/get-character.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-character?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | GET |  |
| [Search Characters](actions/search-characters.md) | GET |  |

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode](actions/get-episode.md) | GET |  |
| [Search Episodes](actions/search-episodes.md) | GET |  |

### Performer

| Action | Method | Description |
| --- | --- | --- |
| [Get Performer](actions/get-performer.md) | GET |  |
| [Search Performers](actions/search-performers.md) | GET |  |

### Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Series](actions/get-series.md) | GET |  |
| [Search Series](actions/search-series.md) | GET |  |

