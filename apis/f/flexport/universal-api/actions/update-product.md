# Flexport: Update Product

Updates an existing product in Flexport.

```
PUT https://connect.mindcloud.co/v1/universal/flexport/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prod_12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexport/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prod_12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique Flexport product ID to update. Example: `prod_12345`. |
| `name` | string | no | Product name. Example: `Organic Cotton T-Shirt`. |
| `sku` | string | no | Product SKU. Example: `SKU-1001`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Product description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "classifications": [
        {}
      ],
      "clientVerified": true,
      "countryOfOrigin": "string",
      "description": "string",
      "hsCodes": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "productCategory": "string",
      "productProperties": [
        {}
      ],
      "sku": "string",
      "suppliers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `classifications` | array<object> |  |
| `clientVerified` | boolean |  |
| `countryOfOrigin` | string |  |
| `description` | string |  |
| `hsCodes` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `productCategory` | string |  |
| `productProperties` | array<object> |  |
| `sku` | string |  |
| `suppliers` | array<object> |  |

## Native endpoint

Through the native Flexport API, this operation is `PATCH /products/:id` (base URL `https://api.flexport.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

