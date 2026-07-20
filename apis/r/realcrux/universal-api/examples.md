# Realcrux Universal API Examples

These examples use the MindCloud API key and Realcrux connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Mail Lists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/list-mail-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/list-mail-lists?${params}`, {
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
      "data": [
        {}
      ],
      "pagination": {},
      "permissions": {}
    }
  ],
  "meta": {}
}
```

See the full [List Mail Lists action reference](actions/list-mail-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/realcrux/latest/actions/list-mail-lists).

## Upsert Subscriber



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/upsert-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_uid": "string",
  "EMAIL": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/upsert-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_uid": "string",
    "EMAIL": "ava@example.com"
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
      "message": "string",
      "status": 1,
      "subscriber_uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Upsert Subscriber action reference](actions/upsert-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/realcrux/latest/actions/upsert-subscriber).
