# Autotask: Create Opportunity



```
POST https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "12345",
  "title": "Managed services renewal",
  "ownerResourceId": "12345",
  "amount": "0",
  "cost": "0",
  "probability": "50",
  "projectedCloseDate": "2026-09-30",
  "stage": "1",
  "status": "1",
  "useQuoteTotals": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "12345",
    "title": "Managed services renewal",
    "ownerResourceId": "12345",
    "amount": "0",
    "cost": "0",
    "probability": "50",
    "projectedCloseDate": "2026-09-30",
    "stage": "1",
    "status": "1",
    "useQuoteTotals": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | The Autotask company for this opportunity. If Contact ID is provided, the contact must be active and belong to this company or its parent. Example: `12345`. |
| `title` | string | yes | The opportunity title. Example: `Managed services renewal`. |
| `ownerResourceId` | number | yes | An active standard Autotask resource with CRM access who owns the opportunity. Example: `12345`. |
| `amount` | number | yes | The opportunity total amount. When revenue-period fields are supplied, Autotask recalculates this value. Example: `0`. |
| `cost` | number | yes | The opportunity total cost. When cost-period fields are supplied, Autotask recalculates this value. Example: `0`. |
| `probability` | number | yes | The close probability as a number from 0 through 100. Example: `50`. |
| `projectedCloseDate` | date | yes | The projected close date in YYYY-MM-DD format. It cannot be earlier than the opportunity create date. Example: `2026-09-30`. |
| `stage` | number | yes | The Autotask opportunity stage value. Example: `1`. |
| `status` | number | yes | The Autotask opportunity status value. Example: `1`. |
| `useQuoteTotals` | boolean | yes | Use quote totals for this opportunity. Set true only when an Autotask quote references the opportunity. |
| `contactId` | number | no | An active contact associated with Company ID or that company's parent. Example: `12345`. |
| `opportunityCategoryId` | number | no | The opportunity category. Autotask applies the selected category's defaults when the opportunity is created. Example: `1`. |
| `organizationalLevelAssociationId` | number | no | The Autotask organizational level association for the opportunity. Example: `12345`. |
| `productId` | number | no | The Autotask product associated with the opportunity. Example: `12345`. |
| `primaryCompetitor` | number | no | The Autotask primary competitor value. Example: `1`. |
| `leadSource` | number | no | The Autotask lead source value. Example: `1`. |
| `rating` | number | no | The Autotask opportunity rating value. Example: `1`. |
| `nextStep` | string | no | The next planned step for the opportunity. Example: `Schedule discovery call`. |
| `description` | string | no | A description of the opportunity. Example: `Opportunity details`. |
| `barriers` | string | no | Barriers that may prevent the opportunity from closing. Example: `Procurement approval`. |
| `helpNeeded` | string | no | Help needed to advance the opportunity. Example: `Technical discovery`. |
| `market` | string | no | The market associated with the opportunity. Example: `Mid-market`. |
| `promotionName` | string | no | The promotion associated with the opportunity. Example: `Summer campaign`. |
| `lossReason` | number | no | The Autotask loss reason value. Example: `1`. |
| `lossReasonDetail` | string | no | Additional detail explaining why the opportunity was lost. Example: `Customer selected another provider`. |
| `lostDate` | date | no | The lost date in YYYY-MM-DD format. Supply it when the opportunity status is Lost. Example: `2026-09-30`. |
| `winReason` | number | no | The Autotask win reason value. Example: `1`. |
| `winReasonDetail` | string | no | Additional detail explaining why the opportunity was won. Example: `Best fit for customer requirements`. |
| `closedDate` | date | no | The closed date in YYYY-MM-DD format. Example: `2026-09-30`. |
| `promisedFulfillmentDate` | date | no | The promised fulfillment date in YYYY-MM-DD format. Example: `2026-10-15`. |
| `throughDate` | date | no | The revenue through date in YYYY-MM-DD format. Example: `2027-09-30`. |
| `revenueSpreadUnit` | string | no | The Autotask revenue spread unit. When both spread fields are omitted, Autotask uses its all-at-once behavior. Example: `month`. |
| `revenueSpread` | number | no | The revenue spread quantity. Autotask discards it when Revenue Spread Unit is omitted. Example: `12`. |
| `totalAmountMonths` | number | no | The total number of months included in the opportunity amount. Example: `12`. |
| `onetimeCost` | number | no | One-time cost. Billing-period cost inputs cause Autotask to recalculate total Cost. Example: `0`. |
| `onetimeRevenue` | number | no | One-time revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. Example: `0`. |
| `monthlyCost` | number | no | Monthly cost. Billing-period cost inputs cause Autotask to recalculate total Cost. Example: `0`. |
| `monthlyRevenue` | number | no | Monthly revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. Example: `0`. |
| `quarterlyCost` | number | no | Quarterly cost. Billing-period cost inputs cause Autotask to recalculate total Cost. Example: `0`. |
| `quarterlyRevenue` | number | no | Quarterly revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. Example: `0`. |
| `semiannualCost` | number | no | Semiannual cost. Billing-period cost inputs cause Autotask to recalculate total Cost. Example: `0`. |
| `semiannualRevenue` | number | no | Semiannual revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. Example: `0`. |
| `yearlyCost` | number | no | Yearly cost. Billing-period cost inputs cause Autotask to recalculate total Cost. Example: `0`. |
| `yearlyRevenue` | number | no | Yearly revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. Example: `0`. |
| `advancedField1` | number | no | Autotask opportunity advanced field 1. Example: `Optional value`. |
| `advancedField2` | number | no | Autotask opportunity advanced field 2. Example: `Optional value`. |
| `advancedField3` | number | no | Autotask opportunity advanced field 3. Example: `Optional value`. |
| `advancedField4` | number | no | Autotask opportunity advanced field 4. Example: `Optional value`. |
| `advancedField5` | number | no | Autotask opportunity advanced field 5. Example: `Optional value`. |
| `userDefinedFields[]` | array<object> | no | Optional Autotask opportunity user-defined fields. Multi-select and reference UDFs are not supported by the REST API. |
| `userDefinedFields[].name` | string | no | The exact name of the Autotask user-defined field. Example: `Custom Field Name`. |
| `userDefinedFields[].value` | string | no | The user-defined field value. Example: `Custom field value`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autotask API returns.

## Native endpoint

Through the native Autotask API, this operation is `POST /Opportunities` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

