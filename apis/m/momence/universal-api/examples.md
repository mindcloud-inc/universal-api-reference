# Momence Universal API Examples

These examples use the MindCloud API key and Momence connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/momence/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/momence/latest/actions/list-events?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/momence/latest/actions/list-events).
