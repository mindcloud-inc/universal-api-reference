# EasyPost: Get Order

Retrieves details for an order from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | EasyPost Order ID, beginning with order_. |

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

Through the native EasyPost API, this operation is `GET /orders/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

