# Simpro: Get Catalog Item



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-catalog-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-catalog-item?connectionId=$CONNECTION_ID&companyId=0&catalogId=365" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0",
  "catalogId": "365"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-catalog-item?${params}`, {
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
| `companyId` | string | yes | The Simpro company ID. Example: `0`. |
| `catalogId` | string | yes | The Simpro catalog item ID. Example: `365`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addOnPriceEnabled": true,
      "archived": true,
      "assetTypeId": "string",
      "basePrice": 1,
      "countryOfOrigin": "string",
      "dateModified": "string",
      "displayOrder": 1,
      "estimatedTime": 1,
      "group": {
        "id": 1,
        "name": "Ava Chen",
        "parentGroup": {
          "id": 1,
          "name": "Ava Chen"
        }
      },
      "id": 1,
      "isAsset": true,
      "isFavorite": true,
      "isInventory": true,
      "isMultiCurrency": true,
      "manufacturer": "string",
      "markup": 1,
      "minPackQty": {},
      "name": "Ava Chen",
      "notes": "string",
      "partNo": "string",
      "purchaseTaxCode": {
        "code": "string",
        "id": 1,
        "rate": 1,
        "type": "string"
      },
      "purchasingStage": {},
      "salesTaxCode": {
        "code": "string",
        "id": 1,
        "rate": 1,
        "type": "string"
      },
      "searchTerm": "string",
      "sellPrice": 1,
      "splitPrice": 1,
      "splitPriceEx": 1,
      "splitPriceInc": 1,
      "storageLocation": "string",
      "tradePrice": 1,
      "tradePriceEx": 1,
      "tradePriceInc": 1,
      "tradeSplitQty": 1,
      "uom": {},
      "upc": "string",
      "vendorDescription": "string",
      "vendorQuantity": 1,
      "vendors": [
        {
          "default": true,
          "discount": 1,
          "nettPrice": 1,
          "nettPriceEx": 1,
          "nettPriceInc": 1,
          "splitPriceEx": 1,
          "splitPriceInc": 1,
          "vendor": {
            "id": 1,
            "name": "Ava Chen"
          },
          "vendorPartNo": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addOnPriceEnabled` | boolean |  |
| `archived` | boolean |  |
| `assetTypeId` | string |  |
| `basePrice` | number |  |
| `countryOfOrigin` | string |  |
| `dateModified` | string |  |
| `displayOrder` | number |  |
| `estimatedTime` | number |  |
| `group.id` | number |  |
| `group.name` | string |  |
| `group.parentGroup.id` | number |  |
| `group.parentGroup.name` | string |  |
| `id` | number |  |
| `isAsset` | boolean |  |
| `isFavorite` | boolean |  |
| `isInventory` | boolean |  |
| `isMultiCurrency` | boolean |  |
| `manufacturer` | string |  |
| `markup` | number |  |
| `minPackQty` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `partNo` | string |  |
| `purchaseTaxCode.code` | string |  |
| `purchaseTaxCode.id` | number |  |
| `purchaseTaxCode.rate` | number |  |
| `purchaseTaxCode.type` | string |  |
| `purchasingStage` | object |  |
| `salesTaxCode.code` | string |  |
| `salesTaxCode.id` | number |  |
| `salesTaxCode.rate` | number |  |
| `salesTaxCode.type` | string |  |
| `searchTerm` | string |  |
| `sellPrice` | number |  |
| `splitPrice` | number |  |
| `splitPriceEx` | number |  |
| `splitPriceInc` | number |  |
| `storageLocation` | string |  |
| `tradePrice` | number |  |
| `tradePriceEx` | number |  |
| `tradePriceInc` | number |  |
| `tradeSplitQty` | number |  |
| `uom` | object |  |
| `upc` | string |  |
| `vendorDescription` | string |  |
| `vendorQuantity` | number |  |
| `vendors[].default` | boolean |  |
| `vendors[].discount` | number |  |
| `vendors[].nettPrice` | number |  |
| `vendors[].nettPriceEx` | number |  |
| `vendors[].nettPriceInc` | number |  |
| `vendors[].splitPriceEx` | number |  |
| `vendors[].splitPriceInc` | number |  |
| `vendors[].vendor.id` | number |  |
| `vendors[].vendor.name` | string |  |
| `vendors[].vendorPartNo` | string |  |

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId/catalogs/:catalogId` (base URL `{{credentials.buildUrl}}/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-item.md) for the provider-specific parameters and requirements.

