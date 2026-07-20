# Checkout Page: Get Product

Retrieves a product from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-product?${params}`, {
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
| `productId` | string | yes | Unique identifier. Must be in BSON ObjectId format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "discounts": [
        {}
      ],
      "fileIds": [
        "string"
      ],
      "generateLicenseKeys": true,
      "hasUnlimitedStock": true,
      "id": "string",
      "media": [
        {}
      ],
      "price": {},
      "sku": "string",
      "stock": 1,
      "taxBehavior": "string",
      "taxCode": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "string",
      "variants": [
        {}
      ],
      "variantsRequired": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | When the product was created. |
| `description` | string | Product description as rendered HTML. |
| `discounts` | array<object> | Bulk discounts configured for the product. |
| `fileIds` | array<string> | List of file ids attached to this product. |
| `generateLicenseKeys` | boolean | Whether license keys are generated for purchases of this product. |
| `hasUnlimitedStock` | boolean | Whether stock is unlimited. |
| `id` | string | Unique identifier for the product. |
| `media` | array<object> | Product main image and gallery. |
| `price` | object | Pricing configuration for this product. |
| `sku` | string | Stock keeping unit. |
| `stock` | number | Available stock quantity. |
| `taxBehavior` | string | Tax calculation behavior. |
| `taxCode` | string | Stripe tax code. |
| `title` | string | Product title. |
| `type` | string | Type of product (one-time charge or subscription). |
| `updatedAt` | string | When the product was last updated. |
| `variants` | array<object> | Product variants and options. |
| `variantsRequired` | boolean | Whether variant selection is required. |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/products/:productId` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

