# ADP: List Payroll Allocation Earnings



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-payroll-allocation-earnings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-payroll-allocation-earnings?connectionId=$CONNECTION_ID&limit=25&offset=0&outputId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "outputId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-payroll-allocation-earnings?${params}`, {
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
| `outputId` | string | yes | The payroll output identifier whose associate payment allocation earnings should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternateJobIDs": [
        {
          "idValue": "string",
          "schemeCode": {
            "shortName": "Ava Chen"
          }
        }
      ],
      "associatePayments": [
        {
          "associateOID": "string",
          "payments": [
            {}
          ]
        }
      ],
      "itemID": "string",
      "payrollGroupCode": {
        "codeValue": "string",
        "shortName": "Ava Chen"
      },
      "payrollProcessingJobID": "string",
      "payrollProcessingJobStatusCode": {
        "codeValue": "string",
        "shortName": "Ava Chen"
      },
      "payrollRegionCode": {
        "codeValue": "string"
      },
      "payrollScheduleReference": {
        "payrollRunNumber": "string",
        "payrollScheduleID": "string",
        "payrollWeekNumber": "string",
        "payrollYear": "string",
        "scheduleEntryID": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternateJobIDs` | array<object> |  |
| `alternateJobIDs[].idValue` | string |  |
| `alternateJobIDs[].schemeCode` | object |  |
| `alternateJobIDs[].schemeCode.shortName` | string |  |
| `associatePayments` | array<object> |  |
| `associatePayments[].associateOID` | string |  |
| `associatePayments[].payments` | array<object> |  |
| `itemID` | string |  |
| `payrollGroupCode` | object |  |
| `payrollGroupCode.codeValue` | string |  |
| `payrollGroupCode.shortName` | string |  |
| `payrollProcessingJobID` | string |  |
| `payrollProcessingJobStatusCode` | object |  |
| `payrollProcessingJobStatusCode.codeValue` | string |  |
| `payrollProcessingJobStatusCode.shortName` | string |  |
| `payrollRegionCode` | object |  |
| `payrollRegionCode.codeValue` | string |  |
| `payrollScheduleReference` | object |  |
| `payrollScheduleReference.payrollRunNumber` | string |  |
| `payrollScheduleReference.payrollScheduleID` | string |  |
| `payrollScheduleReference.payrollWeekNumber` | string |  |
| `payrollScheduleReference.payrollYear` | string |  |
| `payrollScheduleReference.scheduleEntryID` | string |  |

## Native endpoint

Through the native ADP API, this operation is `GET payroll/v2/payroll-output/:outputId/associate-payment-allocations/earnings` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payroll-allocation-earnings.md) for the provider-specific parameters and requirements.

