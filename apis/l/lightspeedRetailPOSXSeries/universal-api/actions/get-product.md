# Lightspeed Retail POS (X-Series): Get Product

Retrieves a product from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-product?${params}`, {
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
| `productId` | string | yes | The Lightspeed product ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCode": "string",
      "accountCodePurchase": "string",
      "active": "string",
      "attributes": "string",
      "brand": "string",
      "brandId": "string",
      "buttonOrder": "string",
      "categories": "string",
      "createdAt": "string",
      "customizations": "string",
      "deletedAt": "string",
      "description": "string",
      "dimensionsUnit": "string",
      "ecwidEnabledWebstore": "string",
      "familyId": "string",
      "handle": "string",
      "hasInventory": "string",
      "hasVariants": "string",
      "height": "string",
      "id": "string",
      "images": "string",
      "imageThumbnailUrl": "https://example.com",
      "imageUrl": "https://example.com",
      "isActive": "string",
      "isComposite": "string",
      "length": "string",
      "loyaltyAmount": "string",
      "name": "Ava Chen",
      "packaging": "string",
      "priceExcludingTax": "string",
      "priceIncludingTax": "string",
      "productCategory": "string",
      "productCodes": "string",
      "productSuppliers": "string",
      "productTypeId": "string",
      "sku": "string",
      "skuImages": "string",
      "source": "string",
      "sourceId": "string",
      "sourceVariantId": "string",
      "supplier": "string",
      "supplierCode": "string",
      "supplierId": "string",
      "supplyPrice": "string",
      "tagIds": "string",
      "type": "string",
      "updatedAt": "string",
      "variantCount": "string",
      "variantName": "Ava Chen",
      "variantOptions": "string",
      "variantParentId": "string",
      "version": "string",
      "weight": "string",
      "weightUnit": "string",
      "width": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCode` | string |  |
| `accountCodePurchase` | string |  |
| `active` | string |  |
| `attributes` | string |  |
| `brand` | string |  |
| `brandId` | string |  |
| `buttonOrder` | string |  |
| `categories` | string |  |
| `createdAt` | string |  |
| `customizations` | string |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `dimensionsUnit` | string |  |
| `ecwidEnabledWebstore` | string |  |
| `familyId` | string |  |
| `handle` | string |  |
| `hasInventory` | string |  |
| `hasVariants` | string |  |
| `height` | string |  |
| `id` | string |  |
| `images` | string |  |
| `imageThumbnailUrl` | string |  |
| `imageUrl` | string |  |
| `isActive` | string |  |
| `isComposite` | string |  |
| `length` | string |  |
| `loyaltyAmount` | string |  |
| `name` | string |  |
| `packaging` | string |  |
| `priceExcludingTax` | string |  |
| `priceIncludingTax` | string |  |
| `productCategory` | string |  |
| `productCodes` | string |  |
| `productSuppliers` | string |  |
| `productTypeId` | string |  |
| `sku` | string |  |
| `skuImages` | string |  |
| `source` | string |  |
| `sourceId` | string |  |
| `sourceVariantId` | string |  |
| `supplier` | string |  |
| `supplierCode` | string |  |
| `supplierId` | string |  |
| `supplyPrice` | string |  |
| `tagIds` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `variantCount` | string |  |
| `variantName` | string |  |
| `variantOptions` | string |  |
| `variantParentId` | string |  |
| `version` | string |  |
| `weight` | string |  |
| `weightUnit` | string |  |
| `width` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/products/:product_id` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

