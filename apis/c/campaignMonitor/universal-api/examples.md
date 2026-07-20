# Campaign Monitor Universal API Examples

These examples use the MindCloud API key and Campaign Monitor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients

Retrieves clients in the authenticated Campaign Monitor account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-clients?${params}`, {
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
      "clientId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignMonitor/latest/actions/list-clients).

## Add Subscriber

Adds a subscriber to a Campaign Monitor list, or updates an existing one.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/add-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "emailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/add-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "emailAddress": "ava@example.com"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber action reference](actions/add-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignMonitor/latest/actions/add-subscriber).
