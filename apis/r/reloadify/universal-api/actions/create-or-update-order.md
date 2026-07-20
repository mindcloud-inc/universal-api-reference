# Reloadify: Create Or Update Order

Creates or updates an order in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "order.id": "string",
  "order.ordered_at": "2026-05-07T12:00:00.000Z",
  "order.profile_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "order.id": "string",
    "order.ordered_at": "2026-05-07T12:00:00.000Z",
    "order.profile_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `order.id` | string | yes | Order identifier. |
| `order.ordered_at` | date | yes | Order timestamp in ISO 8601 format. |
| `order.profile_id` | string | yes | Existing Reloadify profile ID. |

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

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/orders` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-order.md) for the provider-specific parameters and requirements.

