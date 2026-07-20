# Communi App Universal API Examples

These examples use the MindCloud API key and Communi App connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-events?connectionId=$CONNECTION_ID&group=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-events?${params}`, {
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
      "_loadStatus": 1,
      "_rls": 1,
      "communiApp": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "group": 1,
      "id": 1,
      "messageFormatted": "string",
      "titleFormatted": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/communiApp/latest/actions/list-events).
