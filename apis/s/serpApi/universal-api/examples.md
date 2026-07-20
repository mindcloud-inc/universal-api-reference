# SerpApi Universal API Examples

These examples use the MindCloud API key and SerpApi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Google

Retrieves Google search results from SerpApi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-google?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-google?${params}`, {
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
      "displayed_link": "https://example.com",
      "link": "https://example.com",
      "snippet": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Google action reference](actions/search-google.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/serpApi/latest/actions/search-google).
