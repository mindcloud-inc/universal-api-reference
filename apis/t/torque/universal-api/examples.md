# Torque Universal API Examples

These examples use the MindCloud API key and Torque connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Products



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-products?${params}`, {
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
      "category": "string",
      "createdAt": 1,
      "currency": "string",
      "description": "string",
      "id": "string",
      "image": "string",
      "inventory": 1,
      "isSubscription": true,
      "name": "Ava Chen",
      "price": 1,
      "requiresShipping": true,
      "sku": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Products action reference](actions/get-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/torque/latest/actions/get-products).

## Chat With Assistant



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/torque/latest/actions/chat-with-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/torque/latest/actions/chat-with-assistant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}]
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
      "content": "string"
    }
  ],
  "meta": {}
}
```

See the full [Chat With Assistant action reference](actions/chat-with-assistant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/torque/latest/actions/chat-with-assistant).
