# WebinarGeek Universal API Examples

These examples use the MindCloud API key and WebinarGeek connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account Metadata



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-account-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-account-metadata?${params}`, {
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
      "company": "string",
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Account Metadata action reference](actions/retrieve-account-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webinarGeek/latest/actions/retrieve-account-metadata).

## Subscribe to Broadcast



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/subscribe-to-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcastId": 1,
  "firstname": "Ava",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/subscribe-to-broadcast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcastId": 1,
    "firstname": "Ava",
    "email": "ava@example.com"
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
      "confirmationLink": "https://example.com",
      "createdAt": 1,
      "eligibleToWatch": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstname": "Ava",
      "id": 1,
      "unsubscribed": true,
      "watchLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Subscribe to Broadcast action reference](actions/subscribe-to-broadcast.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webinarGeek/latest/actions/subscribe-to-broadcast).
