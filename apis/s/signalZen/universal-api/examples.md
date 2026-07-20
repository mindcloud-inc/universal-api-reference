# SignalZen Universal API Examples

These examples use the MindCloud API key and SignalZen connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from SignalZen.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/list-users?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "last_url": "https://example.com",
      "name": "Ava Chen",
      "online_at": "2026-05-07T12:00:00.000Z",
      "reference": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_attributes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signalZen/latest/actions/list-users).
