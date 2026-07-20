# ClickHouse Universal API Examples

These examples use the MindCloud API key and ClickHouse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organizations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-organizations?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enableCoreDumps": true,
      "id": "string",
      "name": "Ava Chen",
      "privateEndpoints": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Organizations action reference](actions/get-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clickHouse/latest/actions/get-organizations).
