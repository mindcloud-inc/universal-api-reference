# Aspire: List Opportunity Service Groups



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-service-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-service-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-service-groups?${params}`, {
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
      "breakEven": 1,
      "displayGroupOnly": true,
      "equipmentExtendedCost": 1,
      "equipmentOverhead": 1,
      "equipmentProfit": 1,
      "extendedCost": 1,
      "extendedHours": 1,
      "extendedPrice": 1,
      "generalConditionsEquipmentExtendedCost": 1,
      "generalConditionsEquipmentExtendedPrice": 1,
      "generalConditionsEquipmentOverhead": 1,
      "generalConditionsLaborExtendedCost": 1,
      "generalConditionsLaborExtendedPrice": 1,
      "generalConditionsLaborOverhead": 1,
      "generalConditionsMaterialExtendedCost": 1,
      "generalConditionsMaterialExtendedPrice": 1,
      "generalConditionsMaterialOverhead": 1,
      "generalConditionsOtherExtendedCost": 1,
      "generalConditionsOtherExtendedPrice": 1,
      "generalConditionsOtherOverhead": 1,
      "generalConditionsSubExtendedCost": 1,
      "generalConditionsSubExtendedPrice": 1,
      "generalConditionsSubOverhead": 1,
      "generalConditionsTotalExtendedCost": 1,
      "generalConditionsTotalExtendedPrice": 1,
      "generalConditionsTotalOverhead": 1,
      "groupDescription": {},
      "groupName": "Ava Chen",
      "laborExtendedCost": 1,
      "laborOverhead": 1,
      "laborProfit": 1,
      "materialExtendedCost": 1,
      "materialOverhead": 1,
      "materialProfit": 1,
      "opportunityID": 1,
      "opportunityServiceGroupID": 1,
      "optionalServiceGroup": true,
      "otherExtendedCost": 1,
      "otherOverhead": 1,
      "otherProfit": 1,
      "overhead": 1,
      "perPrice": 1,
      "serviceItemQuantity": 1,
      "sortOrder": 1,
      "subExtendedCost": 1,
      "subOverhead": 1,
      "subProfit": 1,
      "taxableExtendedPrice": 1,
      "tMPerServiceExtendedPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakEven` | number |  |
| `displayGroupOnly` | boolean |  |
| `equipmentExtendedCost` | number |  |
| `equipmentOverhead` | number |  |
| `equipmentProfit` | number |  |
| `extendedCost` | number |  |
| `extendedHours` | number |  |
| `extendedPrice` | number |  |
| `generalConditionsEquipmentExtendedCost` | number |  |
| `generalConditionsEquipmentExtendedPrice` | number |  |
| `generalConditionsEquipmentOverhead` | number |  |
| `generalConditionsLaborExtendedCost` | number |  |
| `generalConditionsLaborExtendedPrice` | number |  |
| `generalConditionsLaborOverhead` | number |  |
| `generalConditionsMaterialExtendedCost` | number |  |
| `generalConditionsMaterialExtendedPrice` | number |  |
| `generalConditionsMaterialOverhead` | number |  |
| `generalConditionsOtherExtendedCost` | number |  |
| `generalConditionsOtherExtendedPrice` | number |  |
| `generalConditionsOtherOverhead` | number |  |
| `generalConditionsSubExtendedCost` | number |  |
| `generalConditionsSubExtendedPrice` | number |  |
| `generalConditionsSubOverhead` | number |  |
| `generalConditionsTotalExtendedCost` | number |  |
| `generalConditionsTotalExtendedPrice` | number |  |
| `generalConditionsTotalOverhead` | number |  |
| `groupDescription` | object |  |
| `groupName` | string |  |
| `laborExtendedCost` | number |  |
| `laborOverhead` | number |  |
| `laborProfit` | number |  |
| `materialExtendedCost` | number |  |
| `materialOverhead` | number |  |
| `materialProfit` | number |  |
| `opportunityID` | number |  |
| `opportunityServiceGroupID` | number |  |
| `optionalServiceGroup` | boolean |  |
| `otherExtendedCost` | number |  |
| `otherOverhead` | number |  |
| `otherProfit` | number |  |
| `overhead` | number |  |
| `perPrice` | number |  |
| `serviceItemQuantity` | number |  |
| `sortOrder` | number |  |
| `subExtendedCost` | number |  |
| `subOverhead` | number |  |
| `subProfit` | number |  |
| `taxableExtendedPrice` | number |  |
| `tMPerServiceExtendedPrice` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET OpportunityServiceGroups` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunity-service-groups.md) for the provider-specific parameters and requirements.

