# Invoice Ninja: List Products



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-products?${params}`, {
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
| `status` | string | no | Optional status filter such as active, archived, or deleted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Optional related records to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "created_at": 1,
      "documents": [
        {}
      ],
      "id": "string",
      "in_stock_quantity": 1,
      "is_deleted": true,
      "max_quantity": 1,
      "notes": "string",
      "price": 1,
      "product_image": "string",
      "product_key": "string",
      "quantity": 1,
      "stock_notification": true,
      "stock_notification_threshold": 1,
      "tax_id": "string",
      "tax_name1": "Ava Chen",
      "tax_name2": "Ava Chen",
      "tax_name3": "Ava Chen",
      "tax_rate1": 1,
      "tax_rate2": 1,
      "tax_rate3": 1,
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number | Product cost. |
| `created_at` | number | Unix timestamp when the product was created. |
| `documents` | array<object> | Documents attached to the product. |
| `id` | string | Hashed product ID. |
| `in_stock_quantity` | number | Current in-stock quantity. |
| `is_deleted` | boolean | Whether the product is deleted. |
| `max_quantity` | number | Maximum quantity allowed. |
| `notes` | string | Product notes or description. |
| `price` | number | Product price. |
| `product_image` | string | Product image URL or path. |
| `product_key` | string | Invoice Ninja product key. |
| `quantity` | number | Product quantity. |
| `stock_notification` | boolean | Whether stock notifications are enabled. |
| `stock_notification_threshold` | number | Threshold for stock notifications. |
| `tax_id` | string | Associated tax ID. |
| `tax_name1` | string | Primary tax name. |
| `tax_name2` | string | Secondary tax name. |
| `tax_name3` | string | Tertiary tax name. |
| `tax_rate1` | number | Primary tax rate. |
| `tax_rate2` | number | Secondary tax rate. |
| `tax_rate3` | number | Tertiary tax rate. |
| `updated_at` | number | Unix timestamp when the product was last updated. |

## Native endpoint

Through the native Invoice Ninja API, this operation is `GET /products` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

