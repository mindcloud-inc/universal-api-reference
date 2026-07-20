# HeyPoplar: Delete Order

Deletes an order from HeyPoplar.

```
DELETE https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/delete-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/delete-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/delete-order?${params}`, {
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
| `orderId` | string | yes | The ID of the order to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "currency": "string",
      "customer_email_sha256": "ava@example.com",
      "customer_id": "string",
      "id": "string",
      "matched_at": "string",
      "metadata": {},
      "order_date": "string",
      "order_id": "string",
      "organization_id": "string",
      "source": "string",
      "total": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `currency` | string |  |
| `customer_email_sha256` | string |  |
| `customer_id` | string |  |
| `id` | string |  |
| `matched_at` | string |  |
| `metadata` | object |  |
| `order_date` | string |  |
| `order_id` | string |  |
| `organization_id` | string |  |
| `source` | string |  |
| `total` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native HeyPoplar API, this operation is `DELETE /order/:order_id` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order.md) for the provider-specific parameters and requirements.

