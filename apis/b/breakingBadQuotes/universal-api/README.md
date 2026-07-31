# <img src="https://images.mindcloud.co/apps/icons/breaking-bad-quotes_1785426350970.png" alt="Breaking Bad Quotes logo" width="28" height="28"> Breaking Bad Quotes: Universal API

Read public random Breaking Bad quotes and their authors from the unofficial Breaking Bad Quotes API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/breakingBadQuotes/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://breakingbadquotes.xyz/
- **Vendor API docs:** https://github.com/shevabam/breaking-bad-quotes

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Quote](actions/get-random-quote.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quote?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Quote](actions/get-random-quote.md) | GET |  |
| [Get Random Quotes](actions/get-random-quotes.md) | GET |  |

