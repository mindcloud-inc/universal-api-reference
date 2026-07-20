# Hiboutik: Get Product

Retrieves a product from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-product?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-product?${params}`, {
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
| `productId` | string | no | The Hiboutik product id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingAccount": "string",
      "activeSizes": [
        {}
      ],
      "associatedProducts": [
        {}
      ],
      "images": [
        {}
      ],
      "linkedProducts": [
        {}
      ],
      "miscDate": "string",
      "miscDecimal": "string",
      "miscInt": 1,
      "miscText": "string",
      "miscVarchar": "string",
      "miscVarchar2": "string",
      "multiple": 1,
      "pointsIn": 1,
      "pointsOut": 1,
      "productArch": 1,
      "productBarcode": "string",
      "productBckBtnColor": "string",
      "productBrand": 1,
      "productBrandName": "Ava Chen",
      "productCategory": 1,
      "productDesc": "string",
      "productDiscountPrice": "string",
      "productDisplay": 1,
      "productDisplayWww": 1,
      "productFontColor": "string",
      "productId": 1,
      "productModel": "string",
      "productOrder": 1,
      "productPackage": 1,
      "productPrice": "string",
      "productSizeType": 1,
      "productSpecificRules": [
        {}
      ],
      "productsRefExt": "string",
      "productStockManagement": 1,
      "productStorageLocation": "string",
      "productSupplier": 1,
      "productSupplierReference": "string",
      "productSupplyPrice": "string",
      "productVat": 1,
      "productVatValue": "string",
      "shortLabel": "string",
      "stockAvailable": [
        {}
      ],
      "stockAvailableGlobal": 1,
      "tags": [
        {}
      ],
      "updatedAt": "string",
      "weight": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingAccount` | string |  |
| `activeSizes` | array<object> |  |
| `associatedProducts` | array<object> |  |
| `images` | array<object> |  |
| `linkedProducts` | array<object> |  |
| `miscDate` | string |  |
| `miscDecimal` | string |  |
| `miscInt` | number |  |
| `miscText` | string |  |
| `miscVarchar` | string |  |
| `miscVarchar2` | string |  |
| `multiple` | number |  |
| `pointsIn` | number |  |
| `pointsOut` | number |  |
| `productArch` | number |  |
| `productBarcode` | string |  |
| `productBckBtnColor` | string |  |
| `productBrand` | number |  |
| `productBrandName` | string |  |
| `productCategory` | number |  |
| `productDesc` | string |  |
| `productDiscountPrice` | string |  |
| `productDisplay` | number |  |
| `productDisplayWww` | number |  |
| `productFontColor` | string |  |
| `productId` | number |  |
| `productModel` | string |  |
| `productOrder` | number |  |
| `productPackage` | number |  |
| `productPrice` | string |  |
| `productSizeType` | number |  |
| `productSpecificRules` | array<object> |  |
| `productsRefExt` | string |  |
| `productStockManagement` | number |  |
| `productStorageLocation` | string |  |
| `productSupplier` | number |  |
| `productSupplierReference` | string |  |
| `productSupplyPrice` | string |  |
| `productVat` | number |  |
| `productVatValue` | string |  |
| `shortLabel` | string |  |
| `stockAvailable` | array<object> |  |
| `stockAvailableGlobal` | number |  |
| `tags` | array<object> |  |
| `updatedAt` | string |  |
| `weight` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /products/:product_id` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

