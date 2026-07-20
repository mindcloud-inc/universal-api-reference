# Maildroppa Universal API Examples

These examples use the MindCloud API key and Maildroppa connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Subscribers

Counts Maildroppa subscribers by status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-subscribers?${params}`, {
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
      "formattedValue": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

See the full [Count Subscribers action reference](actions/count-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/maildroppa/latest/actions/count-subscribers).

## Add Subscriber Tag By Email



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/add-subscriber-tag-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/add-subscriber-tag-by-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "category": "string",
      "id": "string",
      "name": "Ava Chen",
      "systemTag": true,
      "userTag": true
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber Tag By Email action reference](actions/add-subscriber-tag-by-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/maildroppa/latest/actions/add-subscriber-tag-by-email).
