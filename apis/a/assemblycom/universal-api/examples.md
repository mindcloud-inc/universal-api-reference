# Assembly.com Universal API Examples

These examples use the MindCloud API key and Assembly.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List App Installs

Retrieves app installs in the current Assembly.com workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-app-installs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-app-installs?${params}`, {
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
      "appId": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List App Installs action reference](actions/list-app-installs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assemblycom/latest/actions/list-app-installs).

## Cancel Subscription

Cancels an existing subscription in Assembly.com.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assemblycom/latest/actions/cancel-subscription).
