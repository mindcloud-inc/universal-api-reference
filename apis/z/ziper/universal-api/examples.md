# Ziper Universal API Examples

These examples use the MindCloud API key and Ziper connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get QR Code

Retrieves a WhatsApp login QR code from Ziper.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziper/latest/actions/get-qr-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziper/latest/actions/get-qr-code?${params}`, {
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
      "base64": "https://example.com",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get QR Code action reference](actions/get-qr-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ziper/latest/actions/get-qr-code).

## Send Buttons

Sends a WhatsApp button message with Ziper.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ziper/latest/actions/send-buttons" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string",
  "text": "string",
  "buttons[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ziper/latest/actions/send-buttons', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string",
    "text": "string",
    "buttons[]": [{}]
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Buttons action reference](actions/send-buttons.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ziper/latest/actions/send-buttons).
