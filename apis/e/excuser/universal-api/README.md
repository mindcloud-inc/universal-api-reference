# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423700130.png" alt="Excuser logo" width="28" height="28"> Excuser: Universal API

Excuser through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/excuser/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Excuse By ID](actions/fetch-excuse-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/excuser/latest/actions/fetch-excuse-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Excuse

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Excuse By ID](actions/fetch-excuse-by-id.md) | GET |  |
| [Fetch Random Excuse](actions/fetch-random-excuse.md) | GET |  |
| [Fetch Random Excuse By Category](actions/fetch-random-excuse-by-category.md) | GET |  |
| [Fetch Random Excuses](actions/fetch-random-excuses.md) | GET |  |
| [Fetch Random Excuses By Category](actions/fetch-random-excuses-by-category.md) | GET |  |

