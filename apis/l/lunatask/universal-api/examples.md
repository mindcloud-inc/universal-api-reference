# Lunatask Universal API Examples

These examples use the MindCloud API key and Lunatask connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/ping?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Ping action reference](actions/ping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lunatask/latest/actions/ping).

## Create Journal Entry



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-journal-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateOn": "2026-05-07T12:00:00.000Z",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-journal-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateOn": "2026-05-07T12:00:00.000Z",
    "content": "string"
  })
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
      "dateOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Journal Entry action reference](actions/create-journal-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lunatask/latest/actions/create-journal-entry).
