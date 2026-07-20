# Reloadify: Get Order

Retrieves an order from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-order?connectionId=$CONNECTION_ID&languageId=string&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageId": "string",
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-order?${params}`, {
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
| `languageId` | string | yes | Reloadify language ID. |
| `orderId` | string | yes | Order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkout_id": "string",
      "created_at": "string",
      "currency": "string",
      "custom_attributes": [
        {}
      ],
      "discount_code": "string",
      "id": "string",
      "is_discount_applied": true,
      "number": "string",
      "ordered_at": "string",
      "paid": true,
      "price": 1,
      "product_ids": [
        "string"
      ],
      "profile_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkout_id` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `custom_attributes` | array<object> |  |
| `discount_code` | string |  |
| `id` | string |  |
| `is_discount_applied` | boolean |  |
| `number` | string |  |
| `ordered_at` | string |  |
| `paid` | boolean |  |
| `price` | number |  |
| `product_ids` | array<string> |  |
| `profile_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/orders/:order_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

