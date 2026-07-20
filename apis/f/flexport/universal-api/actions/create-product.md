# Flexport: Create Product

Creates a new product in Flexport.

```
POST https://connect.mindcloud.co/v1/universal/flexport/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Organic Cotton T-Shirt",
  "sku": "SKU-1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexport/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Organic Cotton T-Shirt",
    "sku": "SKU-1001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Product name. Example: `Organic Cotton T-Shirt`. |
| `sku` | string | yes | Unique product SKU. Example: `SKU-1001`. |

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

Through the native Flexport API, this operation is `POST /products` (base URL `https://api.flexport.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

