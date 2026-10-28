# UKG Ready: List Employee Time Entries



```
GET https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/list-employee-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Ready `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/list-employee-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/list-employee-time-entries?${params}`, {
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
| `startDate` | string | no | minimum date of time entry. Example: 2016-05-01 |
| `endDate` | string | no | maximum date of time entry. Example: 2016-05-30 |
| `companyID` | string | no |  |
| `isLight` | boolean | no | Use light request containing only raw time entry data, no calculated time. |
| `employeeId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employee": {
        "accountId": 1
      },
      "endDate": "string",
      "startDate": "string",
      "timeEntries": [
        {
          "approvalStatus": "string",
          "calcTotal": 1,
          "costCenters": [
            {
              "index": 1,
              "value": {
                "id": 1
              }
            }
          ],
          "date": "string",
          "id": 1,
          "isCalc": true,
          "isRaw": true,
          "total": 1,
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employee.accountId` | number |  |
| `endDate` | string |  |
| `startDate` | string |  |
| `timeEntries[].approvalStatus` | string |  |
| `timeEntries[].calcTotal` | number |  |
| `timeEntries[].costCenters[].index` | number |  |
| `timeEntries[].costCenters[].value.id` | number |  |
| `timeEntries[].date` | string |  |
| `timeEntries[].id` | number |  |
| `timeEntries[].isCalc` | boolean |  |
| `timeEntries[].isRaw` | boolean |  |
| `timeEntries[].total` | number |  |
| `timeEntries[].type` | string |  |

## Native endpoint

Through the native UKG Ready API, this operation is `GET /v2/companies/:cid/employees/:employeeId/time-entries` (base URL `https://{{credentials.hostname}}/ta/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-time-entries.md) for the provider-specific parameters and requirements.

