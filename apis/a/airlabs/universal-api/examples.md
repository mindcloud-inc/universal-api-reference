# Airlabs Universal API Examples

These examples use the MindCloud API key and Airlabs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping Airlabs

Retrieves API status details from Airlabs.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/ping-airlabs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/ping-airlabs?${params}`, {
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
      "request": {},
      "response": "string",
      "terms": "string"
    }
  ],
  "meta": {}
}
```

See the full [Ping Airlabs action reference](actions/ping-airlabs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airlabs/latest/actions/ping-airlabs).

## Create Flight Alert Listener

Creates a flight alert listener in Airlabs.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/create-flight-alert-listener" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/create-flight-alert-listener', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookUrl": "https://example.com"
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
      "listener_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Flight Alert Listener action reference](actions/create-flight-alert-listener.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airlabs/latest/actions/create-flight-alert-listener).
