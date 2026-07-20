# Social Intents Universal API Examples

These examples use the MindCloud API key and Social Intents connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Widgets

Retrieves widgets from Social Intents.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-widgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-widgets?${params}`, {
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
      "created": "string",
      "id": "string",
      "name": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Widgets action reference](actions/list-widgets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/socialIntents/latest/actions/list-widgets).

## Create Chat Completed Webhook

Creates a chat completed webhook in Social Intents.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/create-chat-completed-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "targetUrl": "https://example.com/webhooks/social-intents"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/create-chat-completed-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "targetUrl": "https://example.com/webhooks/social-intents"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Chat Completed Webhook action reference](actions/create-chat-completed-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/socialIntents/latest/actions/create-chat-completed-webhook).
