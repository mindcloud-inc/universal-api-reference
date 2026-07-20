# Smartcar Universal API Examples

These examples use the MindCloud API key and Smartcar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Connections

Retrieves connections from Smartcar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/list-connections?${params}`, {
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
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Connections action reference](actions/list-connections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartcar/latest/actions/list-connections).

## Create Subscription

Creates a new subscription in Smartcar.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "vehicleId": "string",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "vehicleId": "string",
    "webhookId": "string"
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
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Subscription action reference](actions/create-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartcar/latest/actions/create-subscription).
