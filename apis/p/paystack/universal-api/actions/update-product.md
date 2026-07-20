# Paystack: Update Product



```
PUT https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productIdOrCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productIdOrCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productIdOrCode` | string | yes | Enter the numeric Paystack product id. The provider rejects product_code for this endpoint. |
| `name` | string | no |  |
| `description` | string | no |  |
| `price` | number | no |  |
| `currency` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "string",
      "currency": "string",
      "description": "string",
      "id": 1,
      "in_stock": true,
      "name": "Ava Chen",
      "price": 1,
      "product_code": "string",
      "quantity": 1,
      "slug": "string",
      "type": "string",
      "unlimited": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | number |  |
| `in_stock` | boolean |  |
| `name` | string |  |
| `price` | number |  |
| `product_code` | string |  |
| `quantity` | number |  |
| `slug` | string |  |
| `type` | string |  |
| `unlimited` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `PUT /product/:productIdOrCode` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

