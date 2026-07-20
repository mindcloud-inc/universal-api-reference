# Aspire: List Opportunity Service Kit Items

Retrieves opportunity service kit items from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-service-kit-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-service-kit-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-service-kit-items?${params}`, {
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
| `filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AllocationUnitTypeID": 1,
      "AllocationUnitTypeName": "Ava Chen",
      "AvailableToCrew": true,
      "BreakEven": 1,
      "CatalogItemCategoryID": 1,
      "CatalogItemCategoryName": "Ava Chen",
      "CatalogItemID": 1,
      "ExtendedHours": 1,
      "InvertFactor": true,
      "InvertFactorOrig": true,
      "ItemCost": 1,
      "ItemCostExtended": 1,
      "ItemCostOrig": 1,
      "ItemFactor": 1,
      "ItemFactorOrig": 1,
      "ItemName": "Ava Chen",
      "ItemQuantity": 1,
      "ItemQuantityExact": 1,
      "ItemQuantityExtended": 1,
      "ItemQuantityUnit": 1,
      "ItemType": "string",
      "OpportunityID": 1,
      "OpportunityServiceGroupID": 1,
      "OpportunityServiceID": 1,
      "OpportunityServiceItemID": 1,
      "OpportunityServiceKitItemID": 1,
      "Overhead": 1,
      "PerHours": 1,
      "PerHoursOrig": 1,
      "PerPrice": 1,
      "TakeOffItemID": 1,
      "TakeOffItemName": "Ava Chen",
      "UnitPrice": 1,
      "WastePercent": 1,
      "WastePercentOrig": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AllocationUnitTypeID` | number |  |
| `AllocationUnitTypeName` | string |  |
| `AvailableToCrew` | boolean |  |
| `BreakEven` | number |  |
| `CatalogItemCategoryID` | number |  |
| `CatalogItemCategoryName` | string |  |
| `CatalogItemID` | number |  |
| `ExtendedHours` | number |  |
| `InvertFactor` | boolean |  |
| `InvertFactorOrig` | boolean |  |
| `ItemCost` | number |  |
| `ItemCostExtended` | number |  |
| `ItemCostOrig` | number |  |
| `ItemFactor` | number |  |
| `ItemFactorOrig` | number |  |
| `ItemName` | string |  |
| `ItemQuantity` | number |  |
| `ItemQuantityExact` | number |  |
| `ItemQuantityExtended` | number |  |
| `ItemQuantityUnit` | number |  |
| `ItemType` | string |  |
| `OpportunityID` | number |  |
| `OpportunityServiceGroupID` | number |  |
| `OpportunityServiceID` | number |  |
| `OpportunityServiceItemID` | number |  |
| `OpportunityServiceKitItemID` | number |  |
| `Overhead` | number |  |
| `PerHours` | number |  |
| `PerHoursOrig` | number |  |
| `PerPrice` | number |  |
| `TakeOffItemID` | number |  |
| `TakeOffItemName` | string |  |
| `UnitPrice` | number |  |
| `WastePercent` | number |  |
| `WastePercentOrig` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET OpportunityServiceKitItems` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunity-service-kit-items.md) for the provider-specific parameters and requirements.

