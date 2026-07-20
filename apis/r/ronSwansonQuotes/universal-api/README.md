# <img src="https://images.mindcloud.co/apps/icons/ron-swanson-quotes_1777487475615.png" alt="Ron Swanson Quotes logo" width="28" height="28"> Ron Swanson Quotes: Universal API

Public REST API for retrieving random Ron Swanson quotes, multiple quotes, and case-insensitive quote search results from the archived jamesseanwright/ron-swanson-quotes project.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ronSwansonQuotes/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com/jamesseanwright/ron-swanson-quotes
- **Vendor API docs:** https://github.com/jamesseanwright/ron-swanson-quotes

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Quotes](actions/get-quotes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-quotes?connectionId=$CONNECTION_ID&count=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Quotes](actions/get-quotes.md) | GET | Retrieves multiple Ron Swanson quotes. |
| [Get Random Quote](actions/get-random-quote.md) | GET | Retrieves a random Ron Swanson quote. |
| [Search Quotes](actions/search-quotes.md) | GET | Finds Ron Swanson quotes by search term. |

