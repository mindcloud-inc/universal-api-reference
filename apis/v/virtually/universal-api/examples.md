# Virtually Universal API Examples

These examples use the MindCloud API key and Virtually connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization

Retrieves organization details from your Virtually workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-organization?${params}`, {
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
      "color": {},
      "createdAt": 1,
      "description": "string",
      "imageUri": {},
      "isSRM": true,
      "name": "Ava Chen",
      "orgId": "string",
      "ownerEmail": "ava@example.com",
      "ownerPhone": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Organization action reference](actions/get-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/virtually/latest/actions/get-organization).

## Create Action

Creates a new action in Virtually.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": {},
  "message.subject": "string",
  "message.content": "string",
  "channel": {},
  "channel.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": {},
    "message.subject": "string",
    "message.content": "string",
    "channel": {},
    "channel.type": "string"
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
      "actionId": "string",
      "channel": {},
      "description": "string",
      "message": {},
      "name": "Ava Chen",
      "orgId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Action action reference](actions/create-action.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/virtually/latest/actions/create-action).
