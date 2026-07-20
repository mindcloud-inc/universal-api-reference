# Vestaboard Universal API Examples

These examples use the MindCloud API key and Vestaboard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Read Current Message

Retrieves the current message from Vestaboard.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/read-current-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/read-current-message?${params}`, {
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
      "currentMessage": {
        "appeared": 1,
        "id": "string",
        "layout": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Read Current Message action reference](actions/read-current-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vestaboard/latest/actions/read-current-message).

## Send Message

Sends a new message to Vestaboard.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/send-message', {
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
  "data": [
    {
      "created": 1,
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Message action reference](actions/send-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vestaboard/latest/actions/send-message).
