# Pusher Universal API Examples

These examples use the MindCloud API key and Pusher connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Channels

Retrieves channels from Pusher.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channels?${params}`, {
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
      "channels": {}
    }
  ],
  "meta": {}
}
```

See the full [List Channels action reference](actions/list-channels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pusher/latest/actions/list-channels).

## Trigger Batch Events

Triggers multiple events in Pusher.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-batch-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batch[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-batch-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batch[]": [{}]
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
      "batch": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Trigger Batch Events action reference](actions/trigger-batch-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pusher/latest/actions/trigger-batch-events).
