# Excuser Universal API Examples

These examples use the MindCloud API key and Excuser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Excuse By ID



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/excuser/latest/actions/fetch-excuse-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/excuser/latest/actions/fetch-excuse-by-id?${params}`, {
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
      "category": "string",
      "excuse": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Fetch Excuse By ID action reference](actions/fetch-excuse-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/excuser/latest/actions/fetch-excuse-by-id).
