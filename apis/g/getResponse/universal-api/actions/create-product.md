# GetResponse: Create Product

Creates a new product in a GetResponse shop.

```
POST https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shopId": "string",
  "name": "Ava Chen",
  "variants[]": [
    {}
  ],
  "variants[].name": "Ava Chen",
  "variants[].price": 1,
  "variants[].priceTax": 1,
  "variants[].sku": "string",
  "variants[].images[].src": "string",
  "variants[].images[].position": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shopId": "string",
    "name": "Ava Chen",
    "variants[]": [{}],
    "variants[].name": "Ava Chen",
    "variants[].price": 1,
    "variants[].priceTax": 1,
    "variants[].sku": "string",
    "variants[].images[].src": "string",
    "variants[].images[].position": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shopId` | string | yes | The shop ID |
| `name` | string | yes | The product name |
| `variants[]` | array<object> | yes | Product variants collection |
| `type` | string | no | The product type |
| `url` | string | no | External URL for the product |
| `vendor` | string | no | The product vendor |
| `externalId` | string | no | External identifier for the product |
| `categories[]` | array<object> | no | Product categories collection |
| `metaFields[]` | array<object> | no | Product meta fields collection |
| `variants[].name` | string | yes | Variant name |
| `variants[].price` | number | yes | Variant price |
| `variants[].priceTax` | number | yes | Variant price including tax |
| `variants[].sku` | string | yes | Variant SKU |
| `categories[].name` | string | no | Category name |
| `metaFields[].name` | string | no | Meta field name |
| `metaFields[].value` | string | no | Meta field value |
| `metaFields[].valueType` | list<string> | no | Meta field value type One of: `integer`, `string`. |
| `variants[].images[]` | array<object> | no | Variant images collection |
| `variants[].metaFields[]` | array<object> | no | Variant meta fields collection |
| `variants[].taxes[]` | array<object> | no | Variant taxes collection |
| `variants[].images[].src` | string | yes | Source URL for the variant image |
| `variants[].images[].position` | number | yes | Position of the variant image |
| `variants[].metaFields[].name` | string | no | Variant meta field name |
| `variants[].metaFields[].value` | string | no | Variant meta field value |
| `variants[].metaFields[].valueType` | list<string> | no | Variant meta field value type One of: `integer`, `string`. |
| `variants[].metaFields[].description` | string | no | Variant meta field description |
| `variants[].taxes[].name` | string | no | Variant tax name |
| `variants[].taxes[].rate` | number | no | Variant tax rate |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GetResponse API returns.

## Native endpoint

Through the native GetResponse API, this operation is `POST /shops/:shopId/products` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

