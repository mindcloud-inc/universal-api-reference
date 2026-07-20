# SOS Inventory: Update Item

Updates an existing item in SOS Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "syncTokenValue": "string",
  "itemBodyId": 1,
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "syncTokenValue": "string",
    "itemBodyId": 1,
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier for this record. |
| `syncTokenValue` | string | yes | Current version token for this record. |
| `itemBodyId` | number | yes | The item id echoed in the request body. |
| `name` | string | yes | The name of this item. |
| `type` | string | yes | The kind of item. |
| `description` | string | no | Default description of this item. |
| `sku` | string | no | Stockkeeping unit. |
| `notes` | string | no | Any relevant notes for this item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alwaysShippable": true,
      "archived": true,
      "assetAccount": {},
      "available": 1,
      "barcode": "string",
      "basePurchaseCost": {},
      "baseSalesPrice": 1,
      "bin": {},
      "category": {},
      "class": {},
      "cogsAccount": {},
      "commissionAmount": {},
      "commissionExempt": true,
      "commissionRate": {},
      "costBasis": 1,
      "customerPartNumber": "string",
      "customFields": {},
      "description": "string",
      "expenseAccount": {},
      "fullname": "Ava Chen",
      "hasImage": true,
      "hasVariants": true,
      "id": 1,
      "imageAsBase64String": {},
      "imageChanged": true,
      "incomeAccount": {},
      "keys": {},
      "lastSync": "string",
      "leadTime": {},
      "locationBins": {},
      "lotTracking": true,
      "markupPercent": {},
      "maxStock": {},
      "minimumPrice": {},
      "name": "Ava Chen",
      "notes": "string",
      "onhand": 1,
      "onPO": 1,
      "onRMA": 1,
      "onSO": 1,
      "onSR": 1,
      "onWO": 1,
      "pictureFile": {},
      "purchaseCost": 1,
      "purchaseDescription": "string",
      "purchaseTaxCode": {},
      "rented": 1,
      "reorderPoint": {},
      "salesPrice": 1,
      "salesTaxCode": {},
      "serialTracking": true,
      "showOnManufacturingForms": true,
      "showOnPurchasingForms": true,
      "showOnSalesForms": true,
      "sku": "string",
      "starred": 1,
      "sublevel": 1,
      "suggestedQuantity": {},
      "summaryOnly": true,
      "syncMessage": {},
      "syncToken": 1,
      "tags": "string",
      "taxable": true,
      "type": "string",
      "updateBigCommerce": true,
      "updateShopify": true,
      "url": "https://example.com",
      "useMarkup": {},
      "values": {},
      "variantMaster": {},
      "vendor": {},
      "vendorPartNumber": "string",
      "volume": {},
      "volumeUnit": "string",
      "warranty": {},
      "weight": {},
      "weightUnit": "string",
      "willSync": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alwaysShippable` | boolean |  |
| `archived` | boolean |  |
| `assetAccount` | object |  |
| `available` | number |  |
| `barcode` | string |  |
| `basePurchaseCost` | object |  |
| `baseSalesPrice` | number |  |
| `bin` | object |  |
| `category` | object |  |
| `class` | object |  |
| `cogsAccount` | object |  |
| `commissionAmount` | object |  |
| `commissionExempt` | boolean |  |
| `commissionRate` | object |  |
| `costBasis` | number |  |
| `customerPartNumber` | string |  |
| `customFields` | object |  |
| `description` | string |  |
| `expenseAccount` | object |  |
| `fullname` | string |  |
| `hasImage` | boolean |  |
| `hasVariants` | boolean |  |
| `id` | number |  |
| `imageAsBase64String` | object |  |
| `imageChanged` | boolean |  |
| `incomeAccount` | object |  |
| `keys` | object |  |
| `lastSync` | string |  |
| `leadTime` | object |  |
| `locationBins` | object |  |
| `lotTracking` | boolean |  |
| `markupPercent` | object |  |
| `maxStock` | object |  |
| `minimumPrice` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `onhand` | number |  |
| `onPO` | number |  |
| `onRMA` | number |  |
| `onSO` | number |  |
| `onSR` | number |  |
| `onWO` | number |  |
| `pictureFile` | object |  |
| `purchaseCost` | number |  |
| `purchaseDescription` | string |  |
| `purchaseTaxCode` | object |  |
| `rented` | number |  |
| `reorderPoint` | object |  |
| `salesPrice` | number |  |
| `salesTaxCode` | object |  |
| `serialTracking` | boolean |  |
| `showOnManufacturingForms` | boolean |  |
| `showOnPurchasingForms` | boolean |  |
| `showOnSalesForms` | boolean |  |
| `sku` | string |  |
| `starred` | number |  |
| `sublevel` | number |  |
| `suggestedQuantity` | object |  |
| `summaryOnly` | boolean |  |
| `syncMessage` | object |  |
| `syncToken` | number |  |
| `tags` | string |  |
| `taxable` | boolean |  |
| `type` | string |  |
| `updateBigCommerce` | boolean |  |
| `updateShopify` | boolean |  |
| `url` | string |  |
| `useMarkup` | object |  |
| `values` | object |  |
| `variantMaster` | object |  |
| `vendor` | object |  |
| `vendorPartNumber` | string |  |
| `volume` | object |  |
| `volumeUnit` | string |  |
| `warranty` | object |  |
| `weight` | object |  |
| `weightUnit` | string |  |
| `willSync` | boolean |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `PUT /api/v2/item/:id` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

