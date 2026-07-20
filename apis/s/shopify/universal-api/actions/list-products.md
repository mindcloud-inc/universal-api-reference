# Shopify: List Products

Retrieves products from Shopify with GraphQL.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-products?${params}`, {
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
| `query` | string | no | Shopify product search query. Defaults to active products only. Default: `status:active`. Example: `status:active`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `afterCursor` | string | no | Pass previous page endCursor to fetch the next page. |
| `metafieldKeys` | string | no | Optional comma-separated Shopify metafield keys in namespace.key format. When provided, matching metafields are returned for both the product and its variants. Example: `dealer.dealer_product_id, dealer.dealer_variant_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "descriptionHtml": "string",
      "handle": "string",
      "id": "string",
      "images": [
        {
          "altText": "string",
          "src": "string"
        }
      ],
      "metafields": [
        {
          "key": "string",
          "namespace": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "nextCursor": "string",
      "options": [
        {
          "name": "Ava Chen",
          "position": 1,
          "values": [
            "string"
          ]
        }
      ],
      "productType": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "string",
      "variants": [
        {
          "barcode": "string",
          "compareAtPrice": "string",
          "id": "string",
          "inventoryItem": {
            "countryCodeOfOrigin": "string",
            "harmonizedSystemCode": "string",
            "id": "string",
            "unitCost": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "inventoryPolicy": "string",
          "inventoryQuantity": 1,
          "metafields": [
            {
              "key": "string",
              "namespace": "Ava Chen",
              "type": "string",
              "value": "string"
            }
          ],
          "price": "string",
          "selectedOptions": [
            {
              "name": "Ava Chen",
              "value": "string"
            }
          ],
          "sku": "string",
          "taxable": true,
          "title": "string"
        }
      ],
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `descriptionHtml` | string | Product description in HTML. |
| `handle` | string |  |
| `id` | string | Shopify product GID. |
| `images[].altText` | string | Alternative text for product image. |
| `images[].src` | string | Product image source URL. |
| `metafields[].key` | string | Metafield key for the product. |
| `metafields[].namespace` | string | Metafield namespace for the product. |
| `metafields[].type` | string | Metafield type for the product. |
| `metafields[].value` | string | Metafield value for the product. |
| `nextCursor` | string | Cursor to pass into After Cursor for next page. |
| `options[].name` | string |  |
| `options[].position` | number |  |
| `options[].values[]` | string |  |
| `productType` | string |  |
| `status` | string |  |
| `tags[]` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `variants[].barcode` | string |  |
| `variants[].compareAtPrice` | string | Original variant price before discount. |
| `variants[].id` | string |  |
| `variants[].inventoryItem.countryCodeOfOrigin` | string |  |
| `variants[].inventoryItem.harmonizedSystemCode` | string |  |
| `variants[].inventoryItem.id` | string |  |
| `variants[].inventoryItem.unitCost.amount` | string |  |
| `variants[].inventoryItem.unitCost.currencyCode` | string |  |
| `variants[].inventoryPolicy` | string | Inventory policy for out-of-stock behavior. |
| `variants[].inventoryQuantity` | number | Sellable inventory quantity. |
| `variants[].metafields[].key` | string | Metafield key for the variant. |
| `variants[].metafields[].namespace` | string | Metafield namespace for the variant. |
| `variants[].metafields[].type` | string | Metafield type for the variant. |
| `variants[].metafields[].value` | string | Metafield value for the variant. |
| `variants[].price` | string |  |
| `variants[].selectedOptions[].name` | string |  |
| `variants[].selectedOptions[].value` | string |  |
| `variants[].sku` | string |  |
| `variants[].taxable` | boolean | Whether variant is taxable. |
| `variants[].title` | string |  |
| `vendor` | string |  |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

