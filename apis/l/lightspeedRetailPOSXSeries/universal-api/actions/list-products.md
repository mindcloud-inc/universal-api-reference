# Lightspeed Retail POS (X-Series): List Products

Retrieves products from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCode": "string",
      "accountCodePurchase": "string",
      "active": true,
      "attributes": [
        {}
      ],
      "brand": {},
      "brandId": "string",
      "buttonOrder": 1,
      "categories": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customizations": [
        {}
      ],
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dimensionsUnit": "string",
      "ecwidEnabledWebstore": true,
      "familyId": "string",
      "handle": "string",
      "hasInventory": true,
      "hasVariants": true,
      "height": 1,
      "id": "string",
      "images": [
        {}
      ],
      "imageThumbnailUrl": "https://example.com",
      "imageUrl": "https://example.com",
      "isActive": true,
      "isComposite": true,
      "length": 1,
      "loyaltyAmount": 1,
      "name": "Ava Chen",
      "packaging": {},
      "priceExcludingTax": 1,
      "priceIncludingTax": 1,
      "productCategory": {},
      "productCodes": [
        {}
      ],
      "productSuppliers": [
        {}
      ],
      "productTypeId": "string",
      "sku": "string",
      "skuImages": [
        {}
      ],
      "source": "string",
      "sourceId": "string",
      "sourceVariantId": "string",
      "supplier": {},
      "supplierCode": "string",
      "supplierId": "string",
      "supplyPrice": 1,
      "tagIds": [
        "string"
      ],
      "type": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variantCount": 1,
      "variantName": "Ava Chen",
      "variantOptions": [
        {}
      ],
      "variantParentId": "string",
      "version": 1,
      "weight": 1,
      "weightUnit": "string",
      "width": 1
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
| `active` | boolean |  |
| `attributes` | array<object> |  |
| `brand` | object |  |
| `brandId` | string |  |
| `buttonOrder` | number |  |
| `categories` | array<object> |  |
| `createdAt` | date |  |
| `customizations` | array<object> |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `dimensionsUnit` | string |  |
| `ecwidEnabledWebstore` | boolean |  |
| `familyId` | string |  |
| `handle` | string |  |
| `hasInventory` | boolean |  |
| `hasVariants` | boolean |  |
| `height` | number |  |
| `id` | string |  |
| `images` | array<object> |  |
| `imageThumbnailUrl` | string |  |
| `imageUrl` | string |  |
| `isActive` | boolean |  |
| `isComposite` | boolean |  |
| `length` | number |  |
| `loyaltyAmount` | number |  |
| `name` | string |  |
| `packaging` | object |  |
| `priceExcludingTax` | number |  |
| `priceIncludingTax` | number |  |
| `productCategory` | object |  |
| `productCodes` | array<object> |  |
| `productSuppliers` | array<object> |  |
| `productTypeId` | string |  |
| `sku` | string |  |
| `skuImages` | array<object> |  |
| `source` | string |  |
| `sourceId` | string |  |
| `sourceVariantId` | string |  |
| `supplier` | object |  |
| `supplierCode` | string |  |
| `supplierId` | string |  |
| `supplyPrice` | number |  |
| `tagIds` | array<string> |  |
| `type` | object |  |
| `updatedAt` | date |  |
| `variantCount` | number |  |
| `variantName` | string |  |
| `variantOptions` | array<object> |  |
| `variantParentId` | string |  |
| `version` | number |  |
| `weight` | number |  |
| `weightUnit` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/products` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

