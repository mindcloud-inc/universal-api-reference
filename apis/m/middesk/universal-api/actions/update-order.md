# Middesk: Update an order

Updates an order in your Middesk account.

```
PUT https://connect.mindcloud.co/v1/universal/middesk/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the order to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "completedAt": "string",
      "createdAt": "string",
      "id": "string",
      "monitoring": true,
      "object": "string",
      "package": "string",
      "product": "string",
      "requester": {},
      "status": "string",
      "subproducts": [
        "string"
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `monitoring` | boolean |  |
| `object` | string |  |
| `package` | string |  |
| `product` | string |  |
| `requester` | object |  |
| `status` | string |  |
| `subproducts` | array<string> |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `PUT /orders/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

