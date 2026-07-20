# ERPLY Books: Get Products

Retrieves product records from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-products?${params}`, {
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
      "records": [
        {
          "active": 1,
          "added": 1,
          "addedByUsername": "Ava Chen",
          "alcoholPercentage": "string",
          "backbarCharges": 1,
          "batches": "string",
          "brandID": 1,
          "brandName": "Ava Chen",
          "cashierMustEnterPrice": 1,
          "categoryID": 1,
          "categoryName": "Ava Chen",
          "cleanupTimeInMinutes": 1,
          "code": "string",
          "code2": "string",
          "code3": {},
          "containerID": 1,
          "cost": 1,
          "countryOfOriginID": "string",
          "description": "string",
          "descriptionENG": "string",
          "descriptionFIN": "string",
          "descriptionRUS": "string",
          "displayedInWebshop": 1,
          "exciseDeclaration": "string",
          "exciseFermentedProductOver6": "string",
          "exciseFermentedProductUnder6": "string",
          "exciseIntermediateProduct": "string",
          "exciseOtherAlcohol": "string",
          "excisePackaging": "string",
          "exciseWineOver6": "string",
          "grossWeight": "string",
          "groupID": 1,
          "groupName": "Ava Chen",
          "hasQuickSelectButton": 1,
          "hasSerialNumbers": 1,
          "height": "string",
          "isGiftCard": 1,
          "isLotProduct": 1,
          "isRegularGiftCard": 1,
          "isUsedProduct": 1,
          "itemLevelPromotionsDisabled": {},
          "lastModified": 1,
          "lastModifiedByUsername": "Ava Chen",
          "length": "string",
          "lengthInMinutes": 1,
          "locationInWarehouseID": "string",
          "locationInWarehouseName": "Ava Chen",
          "locationInWarehouseText": "string",
          "longdesc": "string",
          "longdescENG": "string",
          "longdescFIN": "string",
          "longdescRUS": "string",
          "manufacturerName": "Ava Chen",
          "name": "Ava Chen",
          "netWeight": "string",
          "nonDiscountable": 1,
          "nonRefundable": 1,
          "nonStockProduct": 1,
          "packagingType": "string",
          "price": 1,
          "priceWithVat": 1,
          "priorityGroupID": "string",
          "productID": 1,
          "registryNumber": "string",
          "reorderMultiple": 1,
          "revenueAccount": "string",
          "rewardPointsNotAllowed": 1,
          "seriesID": 1,
          "seriesName": "Ava Chen",
          "serviceDuration": {},
          "setupTimeInMinutes": 1,
          "shelfLifeDays": 1,
          "soldInPackages": 1,
          "status": "string",
          "supplierCode": {},
          "supplierID": 1,
          "supplierName": {},
          "taxFree": 1,
          "type": "string",
          "unitID": 1,
          "unitName": "Ava Chen",
          "vatrate": 1,
          "vatrateID": 1,
          "volume": "string",
          "walkInService": 1,
          "width": "string"
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].active` | number |  |
| `records[].added` | number |  |
| `records[].addedByUsername` | string |  |
| `records[].alcoholPercentage` | string |  |
| `records[].backbarCharges` | number |  |
| `records[].batches` | string |  |
| `records[].brandID` | number |  |
| `records[].brandName` | string |  |
| `records[].cashierMustEnterPrice` | number |  |
| `records[].categoryID` | number |  |
| `records[].categoryName` | string |  |
| `records[].cleanupTimeInMinutes` | number |  |
| `records[].code` | string |  |
| `records[].code2` | string |  |
| `records[].code3` | object |  |
| `records[].containerID` | number |  |
| `records[].cost` | number |  |
| `records[].countryOfOriginID` | string |  |
| `records[].description` | string |  |
| `records[].descriptionENG` | string |  |
| `records[].descriptionFIN` | string |  |
| `records[].descriptionRUS` | string |  |
| `records[].displayedInWebshop` | number |  |
| `records[].exciseDeclaration` | string |  |
| `records[].exciseFermentedProductOver6` | string |  |
| `records[].exciseFermentedProductUnder6` | string |  |
| `records[].exciseIntermediateProduct` | string |  |
| `records[].exciseOtherAlcohol` | string |  |
| `records[].excisePackaging` | string |  |
| `records[].exciseWineOver6` | string |  |
| `records[].grossWeight` | string |  |
| `records[].groupID` | number |  |
| `records[].groupName` | string |  |
| `records[].hasQuickSelectButton` | number |  |
| `records[].hasSerialNumbers` | number |  |
| `records[].height` | string |  |
| `records[].isGiftCard` | number |  |
| `records[].isLotProduct` | number |  |
| `records[].isRegularGiftCard` | number |  |
| `records[].isUsedProduct` | number |  |
| `records[].itemLevelPromotionsDisabled` | object |  |
| `records[].lastModified` | number |  |
| `records[].lastModifiedByUsername` | string |  |
| `records[].length` | string |  |
| `records[].lengthInMinutes` | number |  |
| `records[].locationInWarehouseID` | string |  |
| `records[].locationInWarehouseName` | string |  |
| `records[].locationInWarehouseText` | string |  |
| `records[].longdesc` | string |  |
| `records[].longdescENG` | string |  |
| `records[].longdescFIN` | string |  |
| `records[].longdescRUS` | string |  |
| `records[].manufacturerName` | string |  |
| `records[].name` | string |  |
| `records[].netWeight` | string |  |
| `records[].nonDiscountable` | number |  |
| `records[].nonRefundable` | number |  |
| `records[].nonStockProduct` | number |  |
| `records[].packagingType` | string |  |
| `records[].price` | number |  |
| `records[].priceWithVat` | number |  |
| `records[].priorityGroupID` | string |  |
| `records[].productID` | number |  |
| `records[].registryNumber` | string |  |
| `records[].reorderMultiple` | number |  |
| `records[].revenueAccount` | string |  |
| `records[].rewardPointsNotAllowed` | number |  |
| `records[].seriesID` | number |  |
| `records[].seriesName` | string |  |
| `records[].serviceDuration` | object |  |
| `records[].setupTimeInMinutes` | number |  |
| `records[].shelfLifeDays` | number |  |
| `records[].soldInPackages` | number |  |
| `records[].status` | string |  |
| `records[].supplierCode` | object |  |
| `records[].supplierID` | number |  |
| `records[].supplierName` | object |  |
| `records[].taxFree` | number |  |
| `records[].type` | string |  |
| `records[].unitID` | number |  |
| `records[].unitName` | string |  |
| `records[].vatrate` | number |  |
| `records[].vatrateID` | number |  |
| `records[].volume` | string |  |
| `records[].walkInService` | number |  |
| `records[].width` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-products.md) for the provider-specific parameters and requirements.

