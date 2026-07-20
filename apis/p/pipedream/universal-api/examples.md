# Pipedream Universal API Examples

These examples use the MindCloud API key and Pipedream connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List apps

Retrieves a list of apps from Pipedream.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/list-apps?${params}`, {
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
      "authType": "string",
      "categories": [
        "string"
      ],
      "connect": {},
      "customFieldsJson": "string",
      "description": "string",
      "featuredWeight": 1,
      "id": "string",
      "imgSrc": "string",
      "name": "Ava Chen",
      "nameSlug": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List apps action reference](actions/list-apps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipedream/latest/actions/list-apps).

## Automatically subscribe a listener to events from new workflows / sources

Creates an auto-subscription for new workflow or source events in Pipedream.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/auto-subscribe-listener-to-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/auto-subscribe-listener-to-events', {
  method: 'POST',
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

See the full [Automatically subscribe a listener to events from new workflows / sources action reference](actions/auto-subscribe-listener-to-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipedream/latest/actions/auto-subscribe-listener-to-events).
