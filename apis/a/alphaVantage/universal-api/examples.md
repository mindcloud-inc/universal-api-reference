# Alpha Vantage Universal API Examples

These examples use the MindCloud API key and Alpha Vantage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Symbols

Finds symbols in Alpha Vantage by keywords.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/search-symbols?connectionId=$CONNECTION_ID&keywords=e.g.%20tesco" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords": "e.g. tesco"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/search-symbols?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "Information": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Symbols action reference](actions/search-symbols.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alphaVantage/latest/actions/search-symbols).
