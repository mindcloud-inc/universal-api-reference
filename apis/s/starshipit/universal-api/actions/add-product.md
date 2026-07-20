# Starshipit: Add Product



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-product', {
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
| `product.sku` | string | no |  |
| `product.title` | string | no |  |
| `product.customsDescription` | string | no |  |
| `product.description` | string | no |  |
| `product.country` | string | no |  |
| `product.weight` | number | no |  |
| `product.height` | number | no |  |
| `product.length` | number | no |  |
| `product.width` | number | no |  |
| `product.hsCode` | string | no |  |
| `product.color` | string | no |  |
| `product.size` | string | no |  |
| `product.barcode` | string | no |  |
| `product.binLocation` | string | no |  |
| `product.brand` | string | no |  |
| `product.usage` | string | no |  |
| `product.material` | string | no |  |
| `product.model` | string | no |  |
| `product.mid` | string | no |  |
| `product.price` | number | no |  |
| `product.dangerousGoodsType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "id": 1,
      "product": {
        "binLocation": "string",
        "color": "string",
        "country": "string",
        "height": 1,
        "hsCode": "string",
        "id": 1,
        "length": 1,
        "price": 1,
        "size": "string",
        "sku": "string",
        "title": "string",
        "weight": 1,
        "width": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `id` | number |  |
| `product` | object |  |
| `product.binLocation` | string |  |
| `product.color` | string |  |
| `product.country` | string |  |
| `product.height` | number |  |
| `product.hsCode` | string |  |
| `product.id` | number |  |
| `product.length` | number |  |
| `product.price` | number |  |
| `product.size` | string |  |
| `product.sku` | string |  |
| `product.title` | string |  |
| `product.weight` | number |  |
| `product.width` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /products` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-product.md) for the provider-specific parameters and requirements.

