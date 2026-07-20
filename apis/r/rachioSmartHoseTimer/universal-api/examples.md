# Rachio Smart Hose Timer Universal API Examples

These examples use the MindCloud API key and Rachio Smart Hose Timer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Person Info

Retrieves the current person identifier from Rachio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-current-person-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-current-person-info?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Person Info action reference](actions/get-current-person-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rachioSmartHoseTimer/latest/actions/get-current-person-info).

## Create Notification Webhook

Creates a notification webhook for a Rachio device.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-notification-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "device.id": "string",
  "url": "https://example.com",
  "eventTypes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-notification-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "device.id": "string",
    "url": "https://example.com",
    "eventTypes[]": [{}]
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

See the full [Create Notification Webhook action reference](actions/create-notification-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rachioSmartHoseTimer/latest/actions/create-notification-webhook).
