# Shopify: List Product Variants

Retrieves product variants from Shopify.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-product-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-product-variants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-product-variants?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | Shopify product variant search query. Leave blank to list variants, or enter any supported productVariants search query such as sku, barcode, product_id, product_status, or updated_at. Example: `sku:TOT-56234286940546`. |
| `updatedAfter` | string | no | Optional modified-date lower bound for Shopify variant search. Appends updated_at:>= to the Product Variant Query. Use YYYY-MM-DD or an ISO timestamp. Example: `2026-05-01`. |
| `updatedBefore` | string | no | Optional modified-date upper bound for Shopify variant search. Appends updated_at:<= to the Product Variant Query. Use YYYY-MM-DD or an ISO timestamp. Example: `2026-06-01`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `afterCursor` | string | no | Pass previous page endCursor to fetch the next page. |
| `metafieldKeys` | string | no | Optional comma-separated Shopify metafield keys in namespace.key format. When provided, matching metafields are returned for both the variant and its parent product. Example: `dealer.dealer_variant_id, dealer.dealer_product_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode": "string",
      "compareAtPrice": "string",
      "createdAt": "string",
      "id": "string",
      "inventoryItem": {
        "countryCodeOfOrigin": "string",
        "harmonizedSystemCode": "string",
        "id": "string",
        "inventoryLevels": {
          "location": {
            "id": "string",
            "name": "Ava Chen"
          },
          "quantities": {
            "name": "Ava Chen",
            "quantity": 1
          }
        },
        "unitCost": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "inventoryPolicy": "string",
      "inventoryQuantity": 1,
      "legacyResourceId": "string",
      "metafields": [
        {
          "key": "string",
          "namespace": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "position": 1,
      "price": "string",
      "product": {
        "createdAt": "string",
        "descriptionHtml": "string",
        "handle": "string",
        "id": "string",
        "images": {
          "altText": "string",
          "src": "string"
        },
        "legacyResourceId": "string",
        "metafields": [
          {
            "key": "string",
            "namespace": "Ava Chen",
            "type": "string",
            "value": "string"
          }
        ],
        "options": {
          "name": "Ava Chen",
          "position": 1,
          "values": [
            "string"
          ]
        },
        "productType": "string",
        "status": "string",
        "tags": [
          "string"
        ],
        "title": "string",
        "updatedAt": "string",
        "vendor": "string"
      },
      "selectedOptions": {
        "name": "Ava Chen",
        "value": "string"
      },
      "sku": "string",
      "taxable": true,
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode` | string |  |
| `compareAtPrice` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `inventoryItem.countryCodeOfOrigin` | string |  |
| `inventoryItem.harmonizedSystemCode` | string |  |
| `inventoryItem.id` | string |  |
| `inventoryItem.inventoryLevels.location.id` | string |  |
| `inventoryItem.inventoryLevels.location.name` | string |  |
| `inventoryItem.inventoryLevels.quantities.name` | string |  |
| `inventoryItem.inventoryLevels.quantities.quantity` | number |  |
| `inventoryItem.unitCost.amount` | string |  |
| `inventoryItem.unitCost.currencyCode` | string |  |
| `inventoryPolicy` | string |  |
| `inventoryQuantity` | number |  |
| `legacyResourceId` | string | Numeric Shopify product variant ID for later search steps. |
| `metafields[].key` | string | Metafield key for the variant. |
| `metafields[].namespace` | string | Metafield namespace for the variant. |
| `metafields[].type` | string | Metafield type for the variant. |
| `metafields[].value` | string | Metafield value for the variant. |
| `position` | number |  |
| `price` | string |  |
| `product.createdAt` | string |  |
| `product.descriptionHtml` | string |  |
| `product.handle` | string |  |
| `product.id` | string |  |
| `product.images.altText` | string |  |
| `product.images.src` | string |  |
| `product.legacyResourceId` | string |  |
| `product.metafields[].key` | string | Metafield key for the parent product. |
| `product.metafields[].namespace` | string | Metafield namespace for the parent product. |
| `product.metafields[].type` | string | Metafield type for the parent product. |
| `product.metafields[].value` | string | Metafield value for the parent product. |
| `product.options.name` | string |  |
| `product.options.position` | number |  |
| `product.options.values` | array<string> |  |
| `product.productType` | string |  |
| `product.status` | string |  |
| `product.tags` | array<string> |  |
| `product.title` | string |  |
| `product.updatedAt` | string |  |
| `product.vendor` | string |  |
| `selectedOptions.name` | string |  |
| `selectedOptions.value` | string |  |
| `sku` | string |  |
| `taxable` | boolean |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-variants.md) for the provider-specific parameters and requirements.

