# Aspire: List Opportunity Services



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-services?${params}`, {
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
      "addedOpportunityRevisionID": {},
      "asNeeded": true,
      "branchID": {},
      "branchName": {},
      "breakEven": 1,
      "changeOrderOpportunityServiceID": {},
      "childOpportunityServiceID": {},
      "complexityPercent": 1,
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "defaultPayCodeID": {},
      "defaultSequenceNumber": {},
      "displayName": "Ava Chen",
      "equipmentExtendedCost": 1,
      "equipmentExtendedPrice": 1,
      "equipmentMarkup": 1,
      "equipmentOverhead": 1,
      "equipmentPerExtendedCost": 1,
      "equipmentPerExtendedPrice": 1,
      "equipmentProfit": 1,
      "equipmentTaxable": true,
      "extendedCost": 1,
      "extendedHours": 1,
      "extendedPrice": 1,
      "invoiceType": "string",
      "laborExtendedCost": 1,
      "laborExtendedPrice": 1,
      "laborMarkup": 1,
      "laborOverhead": 1,
      "laborPerExtendedCost": 1,
      "laborPerExtendedPrice": 1,
      "laborProfit": 1,
      "laborTaxable": true,
      "lastModifiedByUserID": {},
      "lastModifiedByUserName": {},
      "lastModifiedDateTime": {},
      "masterOpportunityServiceID": {},
      "materialExtendedCost": 1,
      "materialExtendedPrice": 1,
      "materialMarkup": 1,
      "materialOverhead": 1,
      "materialPerExtendedCost": 1,
      "materialPerExtendedPrice": 1,
      "materialProfit": 1,
      "materialTaxable": true,
      "minimumPrice": 1,
      "minimumPriceApplied": true,
      "netProfitPercent": 1,
      "occur": {},
      "operationNotes": {},
      "opportunityID": 1,
      "opportunityServiceGroupID": 1,
      "opportunityServiceID": 1,
      "opportunityServiceStatus": "string",
      "otherExtendedCost": 1,
      "otherExtendedPrice": 1,
      "otherMarkup": 1,
      "otherOverhead": 1,
      "otherPerExtendedCost": 1,
      "otherPerExtendedPrice": 1,
      "otherProfit": 1,
      "otherTaxable": true,
      "overhead": 1,
      "overridePrice": true,
      "overridePricing": true,
      "parentOpportunityServiceID": {},
      "perCost": 1,
      "perHours": 1,
      "perHoursOrig": 1,
      "perPrice": 1,
      "perPriceOverride": {},
      "perVisitHours": 1,
      "perVisitMaterialsQty": 1,
      "removedOpportunityRevisionID": {},
      "revisionStartWorkTicketID": {},
      "roundPrice": true,
      "separateWorkTicket": true,
      "serviceDescription": {},
      "serviceID": 1,
      "serviceItemQuantity": 1,
      "serviceNameAbrOverride": {},
      "sortOrder": 1,
      "subExtendedCost": 1,
      "subExtendedPrice": 1,
      "subMarkup": 1,
      "subOverhead": 1,
      "subPerExtendedCost": 1,
      "subPerExtendedPrice": 1,
      "subProfit": 1,
      "subTaxable": true,
      "taxableExtendedPrice": 1,
      "taxablePerExtendedPrice": 1,
      "tMEquipmentMarkupPercent": 1,
      "tMMaterialMarkupPercent": 1,
      "tMMinimumHours": {},
      "tMOtherMarkupPercent": 1,
      "tMSubMarkupPercent": 1,
      "workersCompCode": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedOpportunityRevisionID` | object |  |
| `asNeeded` | boolean |  |
| `branchID` | object |  |
| `branchName` | object |  |
| `breakEven` | number |  |
| `changeOrderOpportunityServiceID` | object |  |
| `childOpportunityServiceID` | object |  |
| `complexityPercent` | number |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `defaultPayCodeID` | object |  |
| `defaultSequenceNumber` | object |  |
| `displayName` | string |  |
| `equipmentExtendedCost` | number |  |
| `equipmentExtendedPrice` | number |  |
| `equipmentMarkup` | number |  |
| `equipmentOverhead` | number |  |
| `equipmentPerExtendedCost` | number |  |
| `equipmentPerExtendedPrice` | number |  |
| `equipmentProfit` | number |  |
| `equipmentTaxable` | boolean |  |
| `extendedCost` | number |  |
| `extendedHours` | number |  |
| `extendedPrice` | number |  |
| `invoiceType` | string |  |
| `laborExtendedCost` | number |  |
| `laborExtendedPrice` | number |  |
| `laborMarkup` | number |  |
| `laborOverhead` | number |  |
| `laborPerExtendedCost` | number |  |
| `laborPerExtendedPrice` | number |  |
| `laborProfit` | number |  |
| `laborTaxable` | boolean |  |
| `lastModifiedByUserID` | object |  |
| `lastModifiedByUserName` | object |  |
| `lastModifiedDateTime` | object |  |
| `masterOpportunityServiceID` | object |  |
| `materialExtendedCost` | number |  |
| `materialExtendedPrice` | number |  |
| `materialMarkup` | number |  |
| `materialOverhead` | number |  |
| `materialPerExtendedCost` | number |  |
| `materialPerExtendedPrice` | number |  |
| `materialProfit` | number |  |
| `materialTaxable` | boolean |  |
| `minimumPrice` | number |  |
| `minimumPriceApplied` | boolean |  |
| `netProfitPercent` | number |  |
| `occur` | object |  |
| `operationNotes` | object |  |
| `opportunityID` | number |  |
| `opportunityServiceGroupID` | number |  |
| `opportunityServiceID` | number |  |
| `opportunityServiceStatus` | string |  |
| `otherExtendedCost` | number |  |
| `otherExtendedPrice` | number |  |
| `otherMarkup` | number |  |
| `otherOverhead` | number |  |
| `otherPerExtendedCost` | number |  |
| `otherPerExtendedPrice` | number |  |
| `otherProfit` | number |  |
| `otherTaxable` | boolean |  |
| `overhead` | number |  |
| `overridePrice` | boolean |  |
| `overridePricing` | boolean |  |
| `parentOpportunityServiceID` | object |  |
| `perCost` | number |  |
| `perHours` | number |  |
| `perHoursOrig` | number |  |
| `perPrice` | number |  |
| `perPriceOverride` | object |  |
| `perVisitHours` | number |  |
| `perVisitMaterialsQty` | number |  |
| `removedOpportunityRevisionID` | object |  |
| `revisionStartWorkTicketID` | object |  |
| `roundPrice` | boolean |  |
| `separateWorkTicket` | boolean |  |
| `serviceDescription` | object |  |
| `serviceID` | number |  |
| `serviceItemQuantity` | number |  |
| `serviceNameAbrOverride` | object |  |
| `sortOrder` | number |  |
| `subExtendedCost` | number |  |
| `subExtendedPrice` | number |  |
| `subMarkup` | number |  |
| `subOverhead` | number |  |
| `subPerExtendedCost` | number |  |
| `subPerExtendedPrice` | number |  |
| `subProfit` | number |  |
| `subTaxable` | boolean |  |
| `taxableExtendedPrice` | number |  |
| `taxablePerExtendedPrice` | number |  |
| `tMEquipmentMarkupPercent` | number |  |
| `tMMaterialMarkupPercent` | number |  |
| `tMMinimumHours` | object |  |
| `tMOtherMarkupPercent` | number |  |
| `tMSubMarkupPercent` | number |  |
| `workersCompCode` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET OpportunityServices` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunity-services.md) for the provider-specific parameters and requirements.

