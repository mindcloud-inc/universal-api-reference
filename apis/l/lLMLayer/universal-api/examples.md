# LLMLayer Universal API Examples

These examples use the MindCloud API key and LLMLayer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Web

Searches the web in LLMLayer for raw results.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web?connectionId=$CONNECTION_ID&query=Search%20query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Search query"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web?${params}`, {
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
      "cost": 1,
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Search Web action reference](actions/search-web.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lLMLayer/latest/actions/search-web).
