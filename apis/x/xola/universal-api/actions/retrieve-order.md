# Xola: Retrieve Order

Retrieves an order from Xola by ID.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-order?${params}`, {
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
| `id` | string | yes | Order identifier from Xola. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "id": "string"
      },
      "id": "string",
      "items": [
        [
          {}
        ]
      ],
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer.id` | string | Customer identifier. |
| `id` | string | Order identifier. |
| `items[]` | array<object> | Order line items. |
| `object` | string | Xola object type. |
| `status` | string | Order status. |

## Native endpoint

Through the native Xola API, this operation is `GET /orders/{id}` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order.md) for the provider-specific parameters and requirements.

