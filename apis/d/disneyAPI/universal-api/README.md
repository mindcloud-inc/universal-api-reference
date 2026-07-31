# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423559278.png" alt="Disney API logo" width="28" height="28"> Disney API: Universal API

Disney API through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/disneyAPI/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Character](actions/get-character.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | GET |  |
| [List Characters](actions/list-characters.md) | GET |  |

