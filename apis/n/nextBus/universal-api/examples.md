# NextBus Universal API Examples

These examples use the MindCloud API key and NextBus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agencies

Retrieves transit agencies from NextBus.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-agencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-agencies?${params}`, {
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
      "regionTitle": "string",
      "shortTitle": "string",
      "tag": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Agencies action reference](actions/list-agencies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextBus/latest/actions/list-agencies).
