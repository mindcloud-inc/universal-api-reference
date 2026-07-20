# IgnitePost Universal API Examples

These examples use the MindCloud API key and IgnitePost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authenticate

Tests your IgnitePost authentication and returns your account email.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/authenticate?${params}`, {
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
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ignitePost/latest/actions/authenticate).

## Create Order

Creates a new order in IgnitePost.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "font": "string",
  "message": "string",
  "image": "string",
  "recipientAddressOne": "string",
  "recipientCity": "string",
  "recipientState": "string",
  "recipientZip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "font": "string",
    "message": "string",
    "image": "string",
    "recipientAddressOne": "string",
    "recipientCity": "string",
    "recipientState": "string",
    "recipientZip": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "font": "string",
      "id": "string",
      "imageBacksideUrl": "https://example.com",
      "imageInsideUrl": "https://example.com",
      "imageUrl": "https://example.com",
      "insert": "string",
      "letterTemplateId": 1,
      "message": "string",
      "metadata": {},
      "recipientAddressOne": "string",
      "recipientAddressTwo": "string",
      "recipientCity": "string",
      "recipientCompanyName": "Ava Chen",
      "recipientCountry": "string",
      "recipientEmail": "ava@example.com",
      "recipientName": "Ava Chen",
      "recipientState": "string",
      "recipientZip": "string",
      "senderAddressOne": "string",
      "senderAddressTwo": "string",
      "senderCity": "string",
      "senderCountry": "string",
      "senderName": "Ava Chen",
      "senderState": "string",
      "senderZip": "string",
      "sendOn": "2026-05-07T12:00:00.000Z",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ignitePost/latest/actions/create-order).
