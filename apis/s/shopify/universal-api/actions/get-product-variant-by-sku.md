# Shopify: Get Product Variant by SKU

Finds product variants in Shopify by SKU.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-product-variant-by-sku
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-product-variant-by-sku?connectionId=$CONNECTION_ID&variables.query=SKU-1-EXAMPLE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.query": "SKU-1-EXAMPLE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-product-variant-by-sku?${params}`, {
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
| `variables` | object | no |  |
| `variables.query` | string | yes | Exact Shopify SKU. The action automatically applies Shopify's sku: search filter. Example: `SKU-1-EXAMPLE`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | A GraphQL query to find a product by it's SKU. Default: `query VariantBySku($first: Int!, $query: String!) {   productVariants(first: $first, query: $query) {     edges {       node {         id           legacyResourceId           sku         title         price         inventoryQuantity         product {           id           legacyResourceId           title           handle         }         inventoryItem {           id           legacyResourceId           inventoryLevels(first: 10) {             edges {               node {                 location {                   id                   name                 }                 quantities(names: [\"available\"]) {                   name                   quantity                 }               }             }           }         }       }     }   } }`. |

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
        "tracked": true,
        "unitCost": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "inventoryPolicy": "string",
      "inventoryQuantity": 1,
      "price": "string",
      "product": {
        "handle": "string",
        "id": "string",
        "status": "string",
        "title": "string",
        "vendor": "string"
      },
      "selectedOptions": [
        {
          "name": "Ava Chen",
          "value": "string"
        }
      ],
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
| `barcode` | string | Variant barcode. |
| `compareAtPrice` | string | Original variant price before discount. |
| `createdAt` | string | Variant creation timestamp. |
| `id` | string | Shopify product variant GID. |
| `inventoryItem.countryCodeOfOrigin` | string | Country of origin for the inventory item. |
| `inventoryItem.harmonizedSystemCode` | string | Harmonized system code for the inventory item. |
| `inventoryItem.id` | string | Shopify inventory item GID. |
| `inventoryItem.tracked` | boolean | Whether the inventory item is tracked. |
| `inventoryItem.unitCost.amount` | string | Inventory unit cost amount. |
| `inventoryItem.unitCost.currencyCode` | string | Inventory unit cost currency. |
| `inventoryPolicy` | string | Out-of-stock behavior for the variant. |
| `inventoryQuantity` | number | Sellable inventory quantity. |
| `price` | string | Variant price. |
| `product.handle` | string | Parent product handle. |
| `product.id` | string | Parent product GID. |
| `product.status` | string | Parent product status. |
| `product.title` | string | Parent product title. |
| `product.vendor` | string | Parent product vendor. |
| `selectedOptions[].name` | string | Variant selected option name. |
| `selectedOptions[].value` | string | Variant selected option value. |
| `sku` | string | Variant SKU. |
| `taxable` | boolean | Whether the variant is taxable. |
| `title` | string | Variant title. |
| `updatedAt` | string | Variant last update timestamp. |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-variant-by-sku.md) for the provider-specific parameters and requirements.

