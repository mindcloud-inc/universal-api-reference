# Aspire: List Oportunity Service Items

Individual equipment, labor/subcontractors, or materials within the scope of a service on an estimate.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-oportunity-service-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-oportunity-service-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-oportunity-service-items?${params}`, {
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
      "allocationUnitTypeID": 1,
      "allocationUnitTypeName": "Ava Chen",
      "breakEven": 1,
      "catalogItemCategoryID": 1,
      "catalogItemCategoryName": "Ava Chen",
      "catalogItemID": {},
      "equipmentExtendedCost": 1,
      "equipmentOverhead": 1,
      "equipmentProfit": 1,
      "estimatingNotes": {},
      "extendedCost": 1,
      "extendedHours": 1,
      "extendedHoursOrig": 1,
      "extendedPrice": 1,
      "forceUnitPricing": {},
      "itemCost": 1,
      "itemCostOrig": 1,
      "itemDescription": {},
      "itemName": "Ava Chen",
      "itemQuantity": 1,
      "itemType": "string",
      "laborExtendedCost": 1,
      "laborOverhead": 1,
      "laborProfit": 1,
      "materialExtendedCost": 1,
      "materialOverhead": 1,
      "materialProfit": 1,
      "occur": {},
      "opportunityServiceID": 1,
      "opportunityServiceItemID": 1,
      "otherExtendedCost": 1,
      "otherOverhead": 1,
      "otherProfit": 1,
      "overhead": 1,
      "overridePrice": true,
      "overrideUnitPrice": true,
      "perHours": 1,
      "perHoursOrig": 1,
      "perPrice": 1,
      "perPriceOverride": 1,
      "sortOrder": 1,
      "subExtendedCost": 1,
      "subOverhead": 1,
      "subProfit": 1,
      "unitPriceOverride": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocationUnitTypeID` | number |  |
| `allocationUnitTypeName` | string |  |
| `breakEven` | number |  |
| `catalogItemCategoryID` | number |  |
| `catalogItemCategoryName` | string |  |
| `catalogItemID` | object |  |
| `equipmentExtendedCost` | number |  |
| `equipmentOverhead` | number |  |
| `equipmentProfit` | number |  |
| `estimatingNotes` | object |  |
| `extendedCost` | number |  |
| `extendedHours` | number |  |
| `extendedHoursOrig` | number |  |
| `extendedPrice` | number |  |
| `forceUnitPricing` | object |  |
| `itemCost` | number |  |
| `itemCostOrig` | number |  |
| `itemDescription` | object |  |
| `itemName` | string |  |
| `itemQuantity` | number |  |
| `itemType` | string |  |
| `laborExtendedCost` | number |  |
| `laborOverhead` | number |  |
| `laborProfit` | number |  |
| `materialExtendedCost` | number |  |
| `materialOverhead` | number |  |
| `materialProfit` | number |  |
| `occur` | object |  |
| `opportunityServiceID` | number |  |
| `opportunityServiceItemID` | number |  |
| `otherExtendedCost` | number |  |
| `otherOverhead` | number |  |
| `otherProfit` | number |  |
| `overhead` | number |  |
| `overridePrice` | boolean |  |
| `overrideUnitPrice` | boolean |  |
| `perHours` | number |  |
| `perHoursOrig` | number |  |
| `perPrice` | number |  |
| `perPriceOverride` | number |  |
| `sortOrder` | number |  |
| `subExtendedCost` | number |  |
| `subOverhead` | number |  |
| `subProfit` | number |  |
| `unitPriceOverride` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET OpportunityServiceItems` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-oportunity-service-items.md) for the provider-specific parameters and requirements.

