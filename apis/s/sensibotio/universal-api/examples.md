# Sensibot.io Universal API Examples

These examples use the MindCloud API key and Sensibot.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Assistant

Retrieves assistant details from Sensibot.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/get-assistant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/get-assistant?${params}`, {
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
        [
          {}
        ]
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Assistant action reference](actions/get-assistant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sensibotio/latest/actions/get-assistant).

## Assistant Bot Type

Updates the assistant bot type in Sensibot.io.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/assistant-bot-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/assistant-bot-type', {
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
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Assistant Bot Type action reference](actions/assistant-bot-type.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sensibotio/latest/actions/assistant-bot-type).
