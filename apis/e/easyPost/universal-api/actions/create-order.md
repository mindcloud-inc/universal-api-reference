# EasyPost: Create Order

Creates a new order in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | object | yes | Order object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isReturn": true,
      "messages": [
        {}
      ],
      "mode": "string",
      "object": "string",
      "rates": [
        {}
      ],
      "reference": "string",
      "shipments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isReturn` | boolean |  |
| `messages` | array<object> |  |
| `mode` | string |  |
| `object` | string |  |
| `rates` | array<object> |  |
| `reference` | string |  |
| `shipments` | array<object> |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /orders` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

