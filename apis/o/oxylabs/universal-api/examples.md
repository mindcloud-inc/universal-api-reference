# Oxylabs Universal API Examples

These examples use the MindCloud API key and Oxylabs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Google Web

Searches Google web results with Oxylabs.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxylabs/latest/actions/search-google-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxylabs/latest/actions/search-google-web?${params}`, {
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
      "job": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Search Google Web action reference](actions/search-google-web.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oxylabs/latest/actions/search-google-web).
