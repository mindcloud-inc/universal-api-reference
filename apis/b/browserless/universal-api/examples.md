# Browserless Universal API Examples

These examples use the MindCloud API key and Browserless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Web

Retrieves web search results from Browserless.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/search-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/search-web?${params}`, {
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
      "data": {},
      "success": true,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

See the full [Search Web action reference](actions/search-web.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browserless/latest/actions/search-web).
