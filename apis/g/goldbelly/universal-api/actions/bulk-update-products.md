# Goldbelly: Bulk Update Products



```
PUT https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products[]": [
    {}
  ],
  "products[].sku": "string",
  "products[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-products', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products[]": [{}],
    "products[].sku": "string",
    "products[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products[]` | array<object> | yes | Products to update. Each item must include SKU and name; price and inventory are optional. |
| `products[].sku` | string | yes | Product SKU. |
| `products[].name` | string | yes | Product name. |
| `products[].price` | number | no | Product price. |
| `products[].inventory` | number | no | Product inventory quantity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "code": 1,
        "message": "string"
      },
      "errors": [
        {
          "sku": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number |  |
| `error.message` | string |  |
| `errors[].sku` | string | 422 response error keyed by SKU when product update fails. |
| `success` | boolean |  |

## Native endpoint

Through the native Goldbelly API, this operation is `POST products/bulk_update` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-products.md) for the provider-specific parameters and requirements.

