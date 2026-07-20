# Paddle Universal API Examples

These examples use the MindCloud API key and Paddle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Event Types

Retrieves a list of event types from Paddle.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/list-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paddle/latest/actions/list-event-types?${params}`, {
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
        {
          "available_versions": [
            1
          ],
          "description": "string",
          "group": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Event Types action reference](actions/list-event-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paddle/latest/actions/list-event-types).

## Cancel Subscription

Cancels an existing subscription in Paddle.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paddle/latest/actions/cancel-subscription', {
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
  "data": [],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paddle/latest/actions/cancel-subscription).
