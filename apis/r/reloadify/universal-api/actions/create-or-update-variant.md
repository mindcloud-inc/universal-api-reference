# Reloadify: Create Or Update Variant

Creates or updates a product variant in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language_id": "string",
  "variant.id": "string",
  "variant.product_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-variant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language_id": "string",
    "variant.id": "string",
    "variant.product_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_id` | string | yes | Language ID from the Reloadify language resource. |
| `variant.id` | string | yes | Variant identifier. |
| `variant.product_id` | string | yes | Existing product ID for the variant. |
| `variant.title` | string | no | Variant title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articleCode": {},
      "createdAt": {},
      "default": true,
      "ean": {},
      "id": "string",
      "mainImage": {},
      "oldPriceExcl": {},
      "oldPriceIncl": {},
      "priceCost": {},
      "priceExcl": {},
      "priceIncl": {},
      "productId": "string",
      "sku": {},
      "stockLevel": {},
      "title": "string",
      "updatedAt": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articleCode` | object |  |
| `createdAt` | object |  |
| `default` | boolean |  |
| `ean` | object |  |
| `id` | string |  |
| `mainImage` | object |  |
| `oldPriceExcl` | object |  |
| `oldPriceIncl` | object |  |
| `priceCost` | object |  |
| `priceExcl` | object |  |
| `priceIncl` | object |  |
| `productId` | string |  |
| `sku` | object |  |
| `stockLevel` | object |  |
| `title` | string |  |
| `updatedAt` | object |  |

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/variants` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-variant.md) for the provider-specific parameters and requirements.

