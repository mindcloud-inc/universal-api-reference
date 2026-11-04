# UKG Pro: Get Earnings History Base Elements

Payroll earnings history base elements for one pay date (page / per_Page).

```
GET https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-earnings-history-base-elements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-earnings-history-base-elements?connectionId=$CONNECTION_ID&payDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-earnings-history-base-elements?${params}`, {
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
| `payDate` | string | yes | Pay date, yyyy-MM-dd. UKG spec types it date-time; the legacy job sends yyyy-MM-dd and 60/60 runs returned rows. |
| `companyID` | string | no |  |
| `employeeID` | string | no |  |
| `employeeNumber` | string | no |  |
| `earningCode` | string | no |  |
| `payGroup` | string | no |  |
| `periodControl` | string | no |  |
| `startPerControl` | string | no |  |
| `endPerControl` | string | no |  |
| `includeInDeferredCompensation` | boolean | no |  |
| `includeInDeferredCompensationHours` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accrualCode": "string",
      "baseAmount": 1,
      "batchID": "string",
      "calculationRule": "string",
      "calculationSequence": "string",
      "companyId": "string",
      "currentAmount": 1,
      "currentHours": 1,
      "earningCode": "string",
      "employeeId": "string",
      "employeeNumber": "string",
      "genNumber": "string",
      "glBaseSegmentId": "string",
      "glFollowBaseAccountAllocation": "string",
      "grossUp": "string",
      "grossUpTarget": 1,
      "grossUpTaxCalculationMethod": 1,
      "hourlyPayRate": 1,
      "includeInDeferredCompensation": true,
      "includeInDeferredCompensationHours": true,
      "isVoided": true,
      "isVoidingRecord": true,
      "jobCode": "string",
      "jobPremiumAmount": 1,
      "jobPremiumRateOrPercent": 1,
      "location": "string",
      "numberOfDays": 1,
      "numberOfGames": 1,
      "payDate": "2026-05-07T12:00:00.000Z",
      "payGroup": "string",
      "payoutRateType": "string",
      "payRate": 1,
      "paySheetID": "string",
      "periodControl": "string",
      "periodPayRate": 1,
      "pieceCount": 1,
      "piecePayRate": 1,
      "planYear": "string",
      "project": "string",
      "reportCategory": "string",
      "taxCalculationGroupId": "string",
      "taxCategory": "string",
      "timeClockCode": "string",
      "tipCredit": 1,
      "tipGrossReceipts": 1,
      "tipType": "string",
      "useDeductionOffSet": true,
      "ytdAmount": 1,
      "ytdShiftAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accrualCode` | string |  |
| `baseAmount` | number |  |
| `batchID` | string |  |
| `calculationRule` | string |  |
| `calculationSequence` | string |  |
| `companyId` | string |  |
| `currentAmount` | number |  |
| `currentHours` | number |  |
| `earningCode` | string |  |
| `employeeId` | string |  |
| `employeeNumber` | string |  |
| `genNumber` | string |  |
| `glBaseSegmentId` | string |  |
| `glFollowBaseAccountAllocation` | string |  |
| `grossUp` | string |  |
| `grossUpTarget` | number |  |
| `grossUpTaxCalculationMethod` | number |  |
| `hourlyPayRate` | number |  |
| `includeInDeferredCompensation` | boolean |  |
| `includeInDeferredCompensationHours` | boolean |  |
| `isVoided` | boolean |  |
| `isVoidingRecord` | boolean |  |
| `jobCode` | string |  |
| `jobPremiumAmount` | number |  |
| `jobPremiumRateOrPercent` | number |  |
| `location` | string |  |
| `numberOfDays` | number |  |
| `numberOfGames` | number |  |
| `payDate` | date |  |
| `payGroup` | string |  |
| `payoutRateType` | string |  |
| `payRate` | number |  |
| `paySheetID` | string |  |
| `periodControl` | string |  |
| `periodPayRate` | number |  |
| `pieceCount` | number |  |
| `piecePayRate` | number |  |
| `planYear` | string |  |
| `project` | string |  |
| `reportCategory` | string |  |
| `taxCalculationGroupId` | string |  |
| `taxCategory` | string |  |
| `timeClockCode` | string |  |
| `tipCredit` | number |  |
| `tipGrossReceipts` | number |  |
| `tipType` | string |  |
| `useDeductionOffSet` | boolean |  |
| `ytdAmount` | number |  |
| `ytdShiftAmount` | number |  |

## Native endpoint

Through the native UKG Pro API, this operation is `GET payroll/v1/earnings-history-base-elements` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-earnings-history-base-elements.md) for the provider-specific parameters and requirements.

