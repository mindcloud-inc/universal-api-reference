# <img src="https://images.mindcloud.co/apps/icons/owen-wilson-wow-api_1785356814169.png" alt="Owen Wilson Wow API logo" width="28" height="28"> Owen Wilson Wow API: Universal API

Retrieve Owen Wilson wow records, chronological selections, and movie/director lists from the public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/owenWilsonWowAPI/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://owen-wilson-wow-api.onrender.com/
- **Vendor API docs:** https://github.com/amamenko/owen-wilson-wow-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Ordered Wow](actions/get-ordered-wow.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/get-ordered-wow?connectionId=$CONNECTION_ID&index=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Director

| Action | Method | Description |
| --- | --- | --- |
| [List Wow Directors](actions/list-wow-directors.md) | GET |  |

### Movie

| Action | Method | Description |
| --- | --- | --- |
| [List Wow Movies](actions/list-wow-movies.md) | GET |  |

### Wow

| Action | Method | Description |
| --- | --- | --- |
| [Get Ordered Wow](actions/get-ordered-wow.md) | GET |  |
| [Get Ordered Wow Range](actions/get-ordered-wow-range.md) | GET |  |
| [Get Random Wows](actions/get-random-wows.md) | GET |  |

