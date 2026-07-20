# Quaderno: Create Product

Creates a new product in Quaderno.

```
POST https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | no | Product code. |
| `description` | string | no | Product description. |
| `kind` | string | no | Whether the product is one-off or subscription. |
| `name` | string | no | Product name. |
| `productType` | string | no | Whether the product is a good or service. |
| `stock` | string | no | Available stock quantity. |
| `taxBasedOn` | string | no | Whether tax is based on customer country or product country. |
| `taxClass` | string | no | Tax class for the product. |
| `taxType` | string | no | Whether tax is included or excluded. |
| `unitCost` | string | no | Unit cost for the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": 1,
      "currency": "string",
      "description": "string",
      "id": 1,
      "kind": "string",
      "name": "Ava Chen",
      "productType": "string",
      "stock": "string",
      "taxBasedOn": "string",
      "taxClass": "string",
      "taxType": "string",
      "unitCost": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | number |  |
| `kind` | string |  |
| `name` | string |  |
| `productType` | string |  |
| `stock` | string |  |
| `taxBasedOn` | string |  |
| `taxClass` | string |  |
| `taxType` | string |  |
| `unitCost` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Quaderno API, this operation is `POST /items` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

