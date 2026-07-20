# AiWifi Universal API Examples

These examples use the MindCloud API key and AiWifi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get webhook events

Retrieves available webhook event types from AiWifi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/get-webhook-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/get-webhook-events?${params}`, {
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
      "code": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get webhook events action reference](actions/get-webhook-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aiWifi/latest/actions/get-webhook-events).

## Create webhook

Creates a new webhook configuration in AiWifi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com",
  "allEvents": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com",
    "allEvents": "true"
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
      "allEvents": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailsToNotify": "ava@example.com",
      "enabled": true,
      "events": [
        "string"
      ],
      "id": 1,
      "name": "Ava Chen",
      "notificationThreshold": "string",
      "secret": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aiWifi/latest/actions/create-webhook).
