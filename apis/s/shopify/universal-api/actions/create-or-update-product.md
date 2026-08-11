# Shopify: Create or Update Product



```
PUT https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-or-update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-or-update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "abc-123",
  "title": "Apple iPhone 14",
  "sku": "ABC-123",
  "price": "799.00",
  "tracked": "true",
  "requiresShipping": "true",
  "inventoryPolicy": "DENY",
  "locationId": "gid://shopify/Location/80529227963",
  "quantity": "9999"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-or-update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "abc-123",
    "title": "Apple iPhone 14",
    "sku": "ABC-123",
    "price": "799.00",
    "tracked": "true",
    "requiresShipping": "true",
    "inventoryPolicy": "DENY",
    "locationId": "gid://shopify/Location/80529227963",
    "quantity": "9999"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `handle` | string | yes | Product handle used as the create-or-update identifier. Example: `abc-123`. |
| `title` | string | yes | Product title. Required so the same action can create a missing product. Example: `Apple iPhone 14`. |
| `sku` | string | yes | SKU for the product's single default variant. Example: `ABC-123`. |
| `price` | number | yes | Base price for the product's single default variant. Example: `799.00`. |
| `tracked` | boolean | yes | Whether Shopify tracks inventory for the variant. Default: `true`. |
| `requiresShipping` | boolean | yes | Whether the variant requires shipping. Default: `true`. |
| `inventoryPolicy` | list<string> | yes | Behavior when inventory reaches zero. One of: `CONTINUE`, `DENY`. Default: `DENY`. |
| `locationId` | list | yes | Shopify location GID where available inventory is set. Example: `gid://shopify/Location/80529227963`. |
| `quantity` | number | yes | Available inventory quantity at the selected location. Example: `9999`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "productSet": {
          "product": {
            "handle": "string",
            "id": "string",
            "title": "string",
            "variants": {
              "nodes": [
                {
                  "compareAtPrice": "string",
                  "id": "string",
                  "inventoryItem": {
                    "id": "string",
                    "requiresShipping": true,
                    "tracked": true
                  },
                  "inventoryPolicy": "string",
                  "inventoryQuantity": 1,
                  "price": "string",
                  "sku": "string"
                }
              ]
            }
          },
          "userErrors": [
            {
              "code": "string",
              "field": [
                "string"
              ],
              "message": "string"
            }
          ]
        }
      },
      "extensions": {
        "cost": {
          "actualQueryCost": 1,
          "requestedQueryCost": 1,
          "throttleStatus": {
            "currentlyAvailable": 1,
            "maximumAvailable": 1,
            "restoreRate": 1
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.productSet.product.handle` | string |  |
| `data.productSet.product.id` | string |  |
| `data.productSet.product.title` | string |  |
| `data.productSet.product.variants.nodes[].compareAtPrice` | string |  |
| `data.productSet.product.variants.nodes[].id` | string |  |
| `data.productSet.product.variants.nodes[].inventoryItem.id` | string |  |
| `data.productSet.product.variants.nodes[].inventoryItem.requiresShipping` | boolean |  |
| `data.productSet.product.variants.nodes[].inventoryItem.tracked` | boolean |  |
| `data.productSet.product.variants.nodes[].inventoryPolicy` | string |  |
| `data.productSet.product.variants.nodes[].inventoryQuantity` | number |  |
| `data.productSet.product.variants.nodes[].price` | string |  |
| `data.productSet.product.variants.nodes[].sku` | string |  |
| `data.productSet.userErrors[].code` | string |  |
| `data.productSet.userErrors[].field` | array<string> |  |
| `data.productSet.userErrors[].message` | string |  |
| `extensions.cost.actualQueryCost` | number |  |
| `extensions.cost.requestedQueryCost` | number |  |
| `extensions.cost.throttleStatus.currentlyAvailable` | number |  |
| `extensions.cost.throttleStatus.maximumAvailable` | number |  |
| `extensions.cost.throttleStatus.restoreRate` | number |  |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-product.md) for the provider-specific parameters and requirements.

