# Reloadify: List Orders

Retrieves orders from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&languageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "languageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-orders?${params}`, {
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
| `created_after` | string | no | Only include orders created after this timestamp. |
| `created_before` | string | no | Only include orders created before this timestamp. |
| `languageId` | string | yes | Reloadify language ID. |
| `updated_after` | string | no | Only include orders updated after this timestamp. |
| `updated_before` | string | no | Only include orders updated before this timestamp. |

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

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/orders` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

