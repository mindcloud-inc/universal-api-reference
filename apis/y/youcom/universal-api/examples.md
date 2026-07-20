# You.com Universal API Examples

These examples use the MindCloud API key and You.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search

Retrieves search results from You.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search?${params}`, {
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
      "metadata": {
        "latency": 1,
        "query": "string",
        "searchUuid": "string"
      },
      "results": {
        "web": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Search action reference](actions/search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youcom/latest/actions/search).
