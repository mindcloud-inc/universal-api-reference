# Aspire: List Catalog Items



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-catalog-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-catalog-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-catalog-items?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allBranches": true,
      "allocateFromMobile": true,
      "allocationUnitTypeID": 1,
      "allocationUnitTypeName": "Ava Chen",
      "availableToBid": true,
      "catalogId": {},
      "catalogItemCategoryID": 1,
      "catalogItemID": 1,
      "catalogName": {},
      "ePAName": {},
      "ePANumber": {},
      "forceUnitPricing": true,
      "inventory": true,
      "itemAlternateName": "Ava Chen",
      "itemCode": {},
      "itemCost": 1,
      "itemDescription": {},
      "itemName": "Ava Chen",
      "itemType": "string",
      "lastUpdatedByUserID": 1,
      "lastUpdatedByUserName": "Ava Chen",
      "lastUpdatedDateTime": "string",
      "materialBarcode1": {},
      "materialBarcode2": {},
      "purchaseUnitCost": 1,
      "purchaseUnitTypeID": 1,
      "purchaseUnitTypeName": "Ava Chen",
      "takeoffItemID": {},
      "unitTypeAllocationConversion": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allBranches` | boolean |  |
| `allocateFromMobile` | boolean |  |
| `allocationUnitTypeID` | number |  |
| `allocationUnitTypeName` | string |  |
| `availableToBid` | boolean |  |
| `catalogId` | object |  |
| `catalogItemCategoryID` | number |  |
| `catalogItemID` | number |  |
| `catalogName` | object |  |
| `ePAName` | object |  |
| `ePANumber` | object |  |
| `forceUnitPricing` | boolean |  |
| `inventory` | boolean |  |
| `itemAlternateName` | string |  |
| `itemCode` | object |  |
| `itemCost` | number |  |
| `itemDescription` | object |  |
| `itemName` | string |  |
| `itemType` | string |  |
| `lastUpdatedByUserID` | number |  |
| `lastUpdatedByUserName` | string |  |
| `lastUpdatedDateTime` | string |  |
| `materialBarcode1` | object |  |
| `materialBarcode2` | object |  |
| `purchaseUnitCost` | number |  |
| `purchaseUnitTypeID` | number |  |
| `purchaseUnitTypeName` | string |  |
| `takeoffItemID` | object |  |
| `unitTypeAllocationConversion` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET CatalogItems` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-catalog-items.md) for the provider-specific parameters and requirements.

