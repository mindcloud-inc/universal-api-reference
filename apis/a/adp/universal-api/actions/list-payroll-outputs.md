# ADP: List Payroll Outputs



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-payroll-outputs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-payroll-outputs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-payroll-outputs?${params}`, {
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
      "alternateJobIDs": [
        {
          "idValue": "string",
          "schemeCode": {
            "shortName": "Ava Chen"
          }
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
| `alternateJobIDs[].idValue` | string |  |
| `alternateJobIDs[].schemeCode.shortName` | string |  |
| `itemID` | string |  |
| `payrollGroupCode.codeValue` | string |  |
| `payrollGroupCode.shortName` | string |  |
| `payrollProcessingJobID` | string |  |
| `payrollProcessingJobStatusCode.codeValue` | string |  |
| `payrollProcessingJobStatusCode.shortName` | string |  |
| `payrollRegionCode.codeValue` | string |  |
| `payrollScheduleReference.payrollRunNumber` | string |  |
| `payrollScheduleReference.payrollScheduleID` | string |  |
| `payrollScheduleReference.payrollWeekNumber` | string |  |
| `payrollScheduleReference.payrollYear` | string |  |
| `payrollScheduleReference.scheduleEntryID` | string |  |

## Native endpoint

Through the native ADP API, this operation is `GET payroll/v2/payroll-output` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payroll-outputs.md) for the provider-specific parameters and requirements.

