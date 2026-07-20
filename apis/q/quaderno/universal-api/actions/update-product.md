# Quaderno: Update Product

Updates an existing product in Quaderno.

```
PUT https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Updated product description. |
| `id` | string | yes | ID of the product to update. |
| `unitCost` | string | no | Updated unit cost. |

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

Through the native Quaderno API, this operation is `PUT /items/:id` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

