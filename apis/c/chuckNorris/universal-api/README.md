# <img src="https://images.mindcloud.co/apps/icons/chuck-norris_1785420692667.png" alt="Chuck Norris logo" width="28" height="28"> Chuck Norris: Universal API

Get random and searchable Chuck Norris facts by category.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chuckNorris/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://api.chucknorris.io
- **Vendor API docs:** https://github.com/chucknorris-io/chuck-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Fact](actions/get-random-fact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/get-random-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Chuck Norris Fact

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Fact](actions/get-random-fact.md) | GET |  |
| [Search Facts](actions/search-facts.md) | GET |  |

### Fact Category

| Action | Method | Description |
| --- | --- | --- |
| [List Fact Categories](actions/list-fact-categories.md) | GET |  |

