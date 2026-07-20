# Queue Universal API Examples

These examples use the MindCloud API key and Queue connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Projects

Retrieves projects from Queue.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-projects?${params}`, {
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
      "archive": "string",
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "private": true,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Projects action reference](actions/get-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/queue/latest/actions/get-projects).

## Cancel Service Checkout

Cancels a service checkout subscription in Queue.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/queue/latest/actions/cancel-service-checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serviceCheckoutId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/queue/latest/actions/cancel-service-checkout', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serviceCheckoutId": "string"
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

See the full [Cancel Service Checkout action reference](actions/cancel-service-checkout.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/queue/latest/actions/cancel-service-checkout).
