# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423680396.png" alt="PoetryDB logo" width="28" height="28"> PoetryDB: Universal API

PoetryDB through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/poetryDB/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Poems by Author](actions/get-poems-by-author.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-author?connectionId=$CONNECTION_ID&author=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Author Discovery

| Action | Method | Description |
| --- | --- | --- |
| [List Authors](actions/list-authors.md) | GET |  |

### Poem

| Action | Method | Description |
| --- | --- | --- |
| [Get Poems by Author](actions/get-poems-by-author.md) | GET |  |
| [Get Poems by Title](actions/get-poems-by-title.md) | GET |  |
| [Get Random Poem](actions/get-random-poem.md) | GET |  |
| [Get Random Poems](actions/get-random-poems.md) | GET |  |

### Title Discovery

| Action | Method | Description |
| --- | --- | --- |
| [List Titles](actions/list-titles.md) | GET |  |

