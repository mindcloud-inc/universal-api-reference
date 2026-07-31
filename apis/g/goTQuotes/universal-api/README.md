# <img src="https://images.mindcloud.co/apps/icons/got-quotes_1785426341181.png" alt="GoT Quotes logo" width="28" height="28"> GoT Quotes: Universal API

Read fan-maintained Game of Thrones quotes and related character and house reference data. Use quote content only in ways that respect applicable franchise rights.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goTQuotes/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Character](actions/get-character.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-character?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | GET |  |
| [List Characters](actions/list-characters.md) | GET |  |

### House

| Action | Method | Description |
| --- | --- | --- |
| [Get House](actions/get-house.md) | GET |  |
| [List Houses](actions/list-houses.md) | GET |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Quote](actions/get-random-quote.md) | GET |  |
| [Get Random Quote by Character](actions/get-random-quote-by-character.md) | GET |  |
| [Get Random Quotes](actions/get-random-quotes.md) | GET |  |
| [Get Random Quotes by Character](actions/get-random-quotes-by-character.md) | GET |  |

