# Invoice Ninja: Update Product



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "productKey": "string",
  "cost": 1,
  "price": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "productKey": "string",
    "cost": 1,
    "price": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Hashed product ID. |
| `productKey` | string | yes | Invoice Ninja product key. |
| `notes` | string | no | Notes or description for the product. |
| `cost` | number | yes | Product cost. |
| `price` | number | yes | Product price. |
| `quantity` | number | no | Product quantity. Default: `1`. |

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

Through the native Invoice Ninja API, this operation is `PUT /products/:id` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

