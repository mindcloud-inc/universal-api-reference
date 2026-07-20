# Aspire: List Opportunities



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunities?${params}`, {
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
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualCostDollars": 1,
      "actualCostLabor": 1,
      "actualCostMaterial": 1,
      "actualCostSub": 1,
      "actualEarnedRevenue": 1,
      "actualGrossMarginDollars": 1,
      "actualGrossMarginPercent": 1,
      "actualLaborCostPerHour": 1,
      "actualLaborHours": 1,
      "anticipatedCloseDate": {},
      "approvedDate": "string",
      "approvedUserID": 1,
      "approvedUserName": "Ava Chen",
      "bidDueDate": {},
      "billingAddressCity": "string",
      "billingAddressID": 1,
      "billingAddressLine1": "string",
      "billingAddressLine2": {},
      "billingAddressStateProvinceCode": "string",
      "billingAddressZipCode": "string",
      "billingCompanyID": 1,
      "billingCompanyName": "Ava Chen",
      "billingContactID": 1,
      "billingContactName": "Ava Chen",
      "branchCode": "string",
      "branchID": 1,
      "branchName": "Ava Chen",
      "budgetedDollars": 1,
      "closedUserID": 1,
      "closedUserName": "Ava Chen",
      "competitorID": {},
      "competitorName": {},
      "completeDate": {},
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "customerContractNum": {},
      "customerPONum": {},
      "districtName": {},
      "divisionCode": "string",
      "divisionID": 1,
      "divisionName": "Ava Chen",
      "electronicPaymentsOverrideConvenienceFee": {},
      "endDate": "string",
      "estimatedBreakEvenDollars": 1,
      "estimatedCostDollars": 1,
      "estimatedDollars": 1,
      "estimatedEquipmentCost": 1,
      "estimatedGrossMarginDollars": 1,
      "estimatedGrossMarginPercent": 1,
      "estimatedLaborCost": 1,
      "estimatedLaborCostPerHour": 1,
      "estimatedLaborHours": 1,
      "estimatedMaterialCost": 1,
      "estimatedNetProfitDollars": 1,
      "estimatedNetProfitPercent": 1,
      "estimatedOtherCost": 1,
      "estimatedOverheadDollars": 1,
      "estimatedRealizeRate": 1,
      "estimatedSubCost": 1,
      "estimatedTotalCost": 1,
      "estimatorNotes": {},
      "federalTaxPercent": 1,
      "invoiceNote": {},
      "invoiceType": "string",
      "jobStatusName": "Ava Chen",
      "leadSourceID": {},
      "leadSourceName": {},
      "lostDate": {},
      "lostReason": {},
      "masterOpportunityID": {},
      "masterOpportunityNumber": {},
      "masterSequenceNum": {},
      "modifiedByUserID": 1,
      "modifiedByUserName": "Ava Chen",
      "modifiedDate": "string",
      "operationsManagerContactID": {},
      "operationsManagerContactName": {},
      "opportunityBillings": [
        {
          "active": true,
          "billMonth": {},
          "invoiceAmount": 1,
          "invoiceDescription": "string",
          "invoiceTriggerPercent": {},
          "opportunityBillingID": 1,
          "opportunityBillingRefID": {},
          "opportunityRevisionID": {},
          "sortOrder": 1
        }
      ],
      "opportunityCanceledReason": {},
      "opportunityCanceledReasonID": {},
      "opportunityID": 1,
      "opportunityName": "Ava Chen",
      "opportunityNumber": 1,
      "opportunityStage": "string",
      "opportunityStageID": 1,
      "opportunityStageName": "Ava Chen",
      "opportunityStatus": "string",
      "opportunityStatusID": 1,
      "opportunityStatusName": "Ava Chen",
      "opportunityType": "string",
      "overridePaymentTerms": {},
      "overridePaymentTermsID": {},
      "paymentTermsID": 1,
      "percentComplete": 1,
      "probability": 1,
      "propertyID": 1,
      "propertyName": "Ava Chen",
      "proposalDescription1": "string",
      "proposalDescription2": "string",
      "proposedDate": "string",
      "proposedUserID": 1,
      "proposedUserName": "Ava Chen",
      "realOpportunityNumber": 1,
      "regionName": {},
      "renewalDate": {},
      "retainageMaturityDate": {},
      "retainagePercent": {},
      "salesRepContactID": 1,
      "salesRepContactName": "Ava Chen",
      "salesTypeID": 1,
      "salesTypeName": "Ava Chen",
      "startDate": "string",
      "stateTaxPercent": 1,
      "taxableAmount": 1,
      "taxablePercent": 1,
      "templateOpportunityID": {},
      "tMPerServiceTaxableAmount": 1,
      "wonDate": "string",
      "wonDollars": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCostDollars` | number |  |
| `actualCostLabor` | number |  |
| `actualCostMaterial` | number |  |
| `actualCostSub` | number |  |
| `actualEarnedRevenue` | number |  |
| `actualGrossMarginDollars` | number |  |
| `actualGrossMarginPercent` | number |  |
| `actualLaborCostPerHour` | number |  |
| `actualLaborHours` | number |  |
| `anticipatedCloseDate` | object |  |
| `approvedDate` | string |  |
| `approvedUserID` | number |  |
| `approvedUserName` | string |  |
| `bidDueDate` | object |  |
| `billingAddressCity` | string |  |
| `billingAddressID` | number |  |
| `billingAddressLine1` | string |  |
| `billingAddressLine2` | object |  |
| `billingAddressStateProvinceCode` | string |  |
| `billingAddressZipCode` | string |  |
| `billingCompanyID` | number |  |
| `billingCompanyName` | string |  |
| `billingContactID` | number |  |
| `billingContactName` | string |  |
| `branchCode` | string |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `budgetedDollars` | number |  |
| `closedUserID` | number |  |
| `closedUserName` | string |  |
| `competitorID` | object |  |
| `competitorName` | object |  |
| `completeDate` | object |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `customerContractNum` | object |  |
| `customerPONum` | object |  |
| `districtName` | object |  |
| `divisionCode` | string |  |
| `divisionID` | number |  |
| `divisionName` | string |  |
| `electronicPaymentsOverrideConvenienceFee` | object |  |
| `endDate` | string |  |
| `estimatedBreakEvenDollars` | number |  |
| `estimatedCostDollars` | number |  |
| `estimatedDollars` | number |  |
| `estimatedEquipmentCost` | number |  |
| `estimatedGrossMarginDollars` | number |  |
| `estimatedGrossMarginPercent` | number |  |
| `estimatedLaborCost` | number |  |
| `estimatedLaborCostPerHour` | number |  |
| `estimatedLaborHours` | number |  |
| `estimatedMaterialCost` | number |  |
| `estimatedNetProfitDollars` | number |  |
| `estimatedNetProfitPercent` | number |  |
| `estimatedOtherCost` | number |  |
| `estimatedOverheadDollars` | number |  |
| `estimatedRealizeRate` | number |  |
| `estimatedSubCost` | number |  |
| `estimatedTotalCost` | number |  |
| `estimatorNotes` | object |  |
| `federalTaxPercent` | number |  |
| `invoiceNote` | object |  |
| `invoiceType` | string |  |
| `jobStatusName` | string |  |
| `leadSourceID` | object |  |
| `leadSourceName` | object |  |
| `lostDate` | object |  |
| `lostReason` | object |  |
| `masterOpportunityID` | object |  |
| `masterOpportunityNumber` | object |  |
| `masterSequenceNum` | object |  |
| `modifiedByUserID` | number |  |
| `modifiedByUserName` | string |  |
| `modifiedDate` | string |  |
| `operationsManagerContactID` | object |  |
| `operationsManagerContactName` | object |  |
| `opportunityBillings[].active` | boolean |  |
| `opportunityBillings[].billMonth` | object |  |
| `opportunityBillings[].invoiceAmount` | number |  |
| `opportunityBillings[].invoiceDescription` | string |  |
| `opportunityBillings[].invoiceTriggerPercent` | object |  |
| `opportunityBillings[].opportunityBillingID` | number |  |
| `opportunityBillings[].opportunityBillingRefID` | object |  |
| `opportunityBillings[].opportunityRevisionID` | object |  |
| `opportunityBillings[].sortOrder` | number |  |
| `opportunityCanceledReason` | object |  |
| `opportunityCanceledReasonID` | object |  |
| `opportunityID` | number |  |
| `opportunityName` | string |  |
| `opportunityNumber` | number |  |
| `opportunityStage` | string |  |
| `opportunityStageID` | number |  |
| `opportunityStageName` | string |  |
| `opportunityStatus` | string |  |
| `opportunityStatusID` | number |  |
| `opportunityStatusName` | string |  |
| `opportunityType` | string |  |
| `overridePaymentTerms` | object |  |
| `overridePaymentTermsID` | object |  |
| `paymentTermsID` | number |  |
| `percentComplete` | number |  |
| `probability` | number |  |
| `propertyID` | number |  |
| `propertyName` | string |  |
| `proposalDescription1` | string |  |
| `proposalDescription2` | string |  |
| `proposedDate` | string |  |
| `proposedUserID` | number |  |
| `proposedUserName` | string |  |
| `realOpportunityNumber` | number |  |
| `regionName` | object |  |
| `renewalDate` | object |  |
| `retainageMaturityDate` | object |  |
| `retainagePercent` | object |  |
| `salesRepContactID` | number |  |
| `salesRepContactName` | string |  |
| `salesTypeID` | number |  |
| `salesTypeName` | string |  |
| `startDate` | string |  |
| `stateTaxPercent` | number |  |
| `taxableAmount` | number |  |
| `taxablePercent` | number |  |
| `templateOpportunityID` | object |  |
| `tMPerServiceTaxableAmount` | number |  |
| `wonDate` | string |  |
| `wonDollars` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Opportunities` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunities.md) for the provider-specific parameters and requirements.

