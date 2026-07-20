# Chatnode Universal API Examples

These examples use the MindCloud API key and Chatnode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authenticate Me



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/authenticate-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/authenticate-me?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate Me action reference](actions/authenticate-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatnode/latest/actions/authenticate-me).

## Send Message



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "message": "string"
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
      "chat_session_id": "string",
      "docs": [
        "string"
      ],
      "id": "string",
      "message": "string",
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Send Message action reference](actions/send-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatnode/latest/actions/send-message).
