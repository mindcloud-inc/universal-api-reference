# Landbot Universal API Examples

These examples use the MindCloud API key and Landbot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Channel

Retrieves a channel from Landbot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-channel?${params}`, {
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
      "active": true,
      "chats": 1,
      "createdAt": 1,
      "hooks": [
        "string"
      ],
      "hsm": 1,
      "id": 1,
      "name": "Ava Chen",
      "token": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Channel action reference](actions/get-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/landbot/latest/actions/get-channel).

## Archive Customer

Archives a customer in Landbot.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/archive-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/landbot/latest/actions/archive-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Archive Customer action reference](actions/archive-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/landbot/latest/actions/archive-customer).
