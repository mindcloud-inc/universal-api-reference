# Logiwa Legacy WMS: List Inventory



```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-inventory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-inventory?${params}`, {
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
| `channelID` | string | no |  |
| `depositorDescription` | string | no |  |
| `pageSize` | string | no |  |
| `selectedPageIndex` | string | no |  |
| `code` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableStockQty": 1,
      "brand": "string",
      "channelDescription": "string",
      "channelID": 1,
      "channelInventoryAmount": 1,
      "channelIsActive": true,
      "channelIsDropShip": true,
      "channelIsExported": true,
      "channelIsNotIncludeInOrder": true,
      "channelItemNumber": "string",
      "channelMasterSellerSku": "string",
      "channelSellerSku": "string",
      "channelUnitPrice": 1,
      "closeToSaleQuantity": 1,
      "code": "string",
      "damagedQuantity": 1,
      "depositorDescription": "string",
      "depositorID": 1,
      "description": "string",
      "detailCategoryDescription": {},
      "fnSku": "string",
      "id": 1,
      "inventorySharingPercentage": 1,
      "isKitItem": true,
      "isOutOfStock": true,
      "lastOnhandQuantitySynced": 1,
      "lastQuantitySynced": 1,
      "lastQuantitySyncedDate": {},
      "lastQuantitySyncedDateEnd": {},
      "lastQuantitySyncedDateStart": {},
      "mainCategoryDescription": {},
      "masterChannelItemNumber": "string",
      "orderQty": 1,
      "pageCount": 1,
      "pageSize": 1,
      "recordCount": 1,
      "selectedPageIndex": 1,
      "sellableStock": 1,
      "shareableQty": 1,
      "storeName": "Ava Chen",
      "usableStock": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableStockQty` | number |  |
| `brand` | string |  |
| `channelDescription` | string |  |
| `channelID` | number |  |
| `channelInventoryAmount` | number |  |
| `channelIsActive` | boolean |  |
| `channelIsDropShip` | boolean |  |
| `channelIsExported` | boolean |  |
| `channelIsNotIncludeInOrder` | boolean |  |
| `channelItemNumber` | string |  |
| `channelMasterSellerSku` | string |  |
| `channelSellerSku` | string |  |
| `channelUnitPrice` | number |  |
| `closeToSaleQuantity` | number |  |
| `code` | string |  |
| `damagedQuantity` | number |  |
| `depositorDescription` | string |  |
| `depositorID` | number |  |
| `description` | string |  |
| `detailCategoryDescription` | object |  |
| `fnSku` | string |  |
| `id` | number |  |
| `inventorySharingPercentage` | number |  |
| `isKitItem` | boolean |  |
| `isOutOfStock` | boolean |  |
| `lastOnhandQuantitySynced` | number |  |
| `lastQuantitySynced` | number |  |
| `lastQuantitySyncedDate` | object |  |
| `lastQuantitySyncedDateEnd` | object |  |
| `lastQuantitySyncedDateStart` | object |  |
| `mainCategoryDescription` | object |  |
| `masterChannelItemNumber` | string |  |
| `orderQty` | number |  |
| `pageCount` | number |  |
| `pageSize` | number |  |
| `recordCount` | number |  |
| `selectedPageIndex` | number |  |
| `sellableStock` | number |  |
| `shareableQty` | number |  |
| `storeName` | string |  |
| `usableStock` | number |  |

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/ListingInventoryReport` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inventory.md) for the provider-specific parameters and requirements.

