# GetResponse: Update Product

Updates an existing product in a GetResponse shop.

```
PUT https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shopId": "string",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shopId": "string",
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shopId` | string | yes | The shop ID |
| `productId` | string | yes | The product ID |
| `name` | string | no | The product name |
| `type` | string | no | The product type |
| `url` | string | no | External URL for the product |
| `vendor` | string | no | The product vendor |
| `externalId` | string | no | External identifier for the product |
| `categories[]` | array<object> | no | Product categories collection |
| `variants[]` | array<object> | no | Product variants collection |
| `metaFields[]` | array<object> | no | Product meta fields collection |
| `variants[].name` | string | no | Variant name |
| `variants[].price` | number | no | Variant price |
| `variants[].priceTax` | number | no | Variant price including tax |
| `variants[].sku` | string | no | Variant SKU |
| `categories[].name` | string | no | Category name |
| `metaFields[].name` | string | no | Meta field name |
| `metaFields[].value` | string | no | Meta field value |
| `metaFields[].valueType` | list<string> | no | Meta field value type One of: `integer`, `string`. |
| `variants[].images[]` | array<object> | no | Variant images collection |
| `variants[].metaFields[]` | array<object> | no | Variant meta fields collection |
| `variants[].taxes[]` | array<object> | no | Variant taxes collection |
| `variants[].images[].src` | string | no | Source URL for the variant image |
| `variants[].images[].position` | number | no | Position of the variant image |
| `variants[].metaFields[].name` | string | no | Variant meta field name |
| `variants[].metaFields[].value` | string | no | Variant meta field value |
| `variants[].metaFields[].valueType` | list<string> | no | Variant meta field value type One of: `integer`, `string`. |
| `variants[].metaFields[].description` | string | no | Variant meta field description |
| `variants[].taxes[].name` | string | no | Variant tax name |
| `variants[].taxes[].rate` | number | no | Variant tax rate |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GetResponse API returns.

## Native endpoint

Through the native GetResponse API, this operation is `POST /shops/:shopId/products/:productId` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

